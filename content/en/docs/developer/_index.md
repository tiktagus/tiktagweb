---
title: "Developer Docs"
linkTitle: "Developer"
categories: ["developer"]
tags: ["developer", "docs"]
weight: 5
draft: true
date: 2022-12-21
description: >
  For design specs, APIs and requirements on https://tiktag.us service

---

{{% pageinfo %}}
  Developer docs are for authorized developers only in private repo https://github.com/tikoly-com/tiktag.us
  Content of this section is the same as this repo's `README.md`.
  End-user features and tutorials are documented on [the open source github repo](https://github.com/tikoly-com/tiktag).
{{% /pageinfo %}}

# tiktag.us

`tiktag.us` is the hosted service for the open source `tiktag` CLI (Command Line Instruction) tool for preparing images for hosting or (authorized) sharing. 

`TikTag` open source is shipped as a local CLI app written in Go. `tiktag.us` is managed by TikTag Core team, part of the _TikolyDAO_.

## Architecture

There are TWO basic components to make `tiktag` works as a CLI app, 

1. The open source `tiktag` CLI runs locally on user's machine
2. The hoseted (none open source) [https://tiktag.us](https://tiktag.us) services, such as `https://i.tiktag.us`, a gRPC service for keeping a global unique ID system for all assets.

## Roadmap

Tiktag was firstly designed to streamline photo preparation before being hosted and published/referenced in a blog post.

### Hosted Features (v0.1)

The hosted service for Tiktag v0.x server offers the following features,

1. Process requests from `tiktag` CLI such as issuing new `ttid` for a new (version of) user asset, such as a photo
2. Authenticate a user's locally run `tiktag` CLI app (instance), once the user has logged in https://tiktag.us with her crypto wallet (such as [Sui Wallet](https://chrome.google.com/webstore/detail/sui-wallet/opcgpfmipidbgpenhmajoajpbobppdil))
   * Note that a user can run as many local `tiktag` instances as she likes
   * each locally run `tiktag` instance has a locally generated `UUID` associated with her wallet ID used for logging into https://tiktag.us
3. Configurable params via `config.yml`, on  

### Hosted Features (v1.x)

_tiktag.us_ v1.x is for commercial uses such as a paying client / partner's. NFT minting adaptors may be implemented according to business needs. We'll see where it'll lead us.

On top of the v0.x features, _tiktag.us_ v1.x may offer the following features,

1. User login with WeChat/Meta/Twitter/Github/..., the traditional web2 OAuth login
2. (Optionally) Support NFT asset verification, as a client app, using APS from same function platforms such as [Gopluslabs.io](https://gopluslabs.io/nft-security-api).
3. User can cherry-pick the ones to be minted as NFT
   * as a response, the minted version shows up along side the original one stored on S3
4. Offer a changelog on an asset's history from its 1st `tiktag` operation until the latest

{{<alert color="warning">}}
We can NOT guarantee the digital copy is the ONLY available one, becuase original creator may keep same copy off tiktag on purposes
{{< /alert >}}

## Tech Stack

Candidate tech dependencies, to be evaluated, for making TikTag happen. 

{{< alert >}}
Shared by both open source and hosted version.
{{< /alert >}}

* Written in Go, using minimal 3rd party libs
* Data store for both CLI and hosted service, [ImmuDB](https://github.com/codenotary/immudb), enforcing immutable data policies
  * more about `ImmuDB` on [this podcast](https://changelog.com/gotime/219).
  * the hosted `ImmuDB` shall be [deployed as a service](https://docs.immudb.io/master/connecting/sdks.html), NOT a lib
* Object storage, S3 API compatible object storage (hosted on [Minio](https://github.com/minio/minio) by default)
* GUI deisgn refence, [RClone (with GUI)](https://rclone.org/gui)
  * `RClone` could be used as a dependency for handling file sync with object storage services 
  * RClone GUI is a web admin for handling `rclone` jobs
