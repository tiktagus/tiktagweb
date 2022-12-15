---
title: "Overview"
linkTitle: "Overview"
weight: 1
description: >
  “Bottom-up digital asset hosting and auditing”
---

## What is TikTag

TikTag is a tool to make digital asset, such as photo, auditable, so that you can,

1. secure trust from others on the ownership and authenticity of the assets,
2. better monetize your digital assets as a creator, such as minting them as NFT,
3. host your digital assets however you like.

{{< alert color="warning" >}}
By design, TikTag **DOES NOT** host your photos or assets. You need to pick your own object storage service and [configure TikTag](/docs/how-to/configure/) properly in order to host them yourself.
{{< /alert >}}

## What TikTag is NOT

TikTag is NOT

* a NFT-minting tool, but we'll integrate TikTag with L2 blockchain such as [Ethereum](https://ethereum.org/) and [Sui Networks](https://sui.io/), or partner apps such as [Gacha](https://gacha.cards/),
* an image editing tool, there are already many such good tools/apps,
* nor a storage service, by design.

## Why do I want TikTag?

We [initially created TikTag](/blog/20221122/why-we-need-to-audit-digital-asset/) to help bloggers and editors to speed up their daily job in hosting photos and images onto object storage like [AWS S3](https://aws.amazon.com/s3/) or [MinIO](https://minio.io/).

Typical TikTag users are working with blogging tools such as [Ghost](https://ghost.org) or [Medium](https://medium.com), on daily basis. They are comfortable with [Markdown](https://www.markdownguide.org/) editors that come with these blogging platforms.

**TikTag is NOT for everyone**, especially for those who are not comfortable with command line apps, such as `Terminal` app in MacOS, to handle your photos or files.

TikTag users are inspired with the following vision,

* _Back to Basics for Efficiency_: command-line is faster than drag-and-drop in handling photos/digital assets, or with any GUI apps.

* _End-to-end Auditable_: from the moment you host your file to the moment you change their ownership, the meta data of your file-handling are logged to our immutable database, such as the `hash` (or `finger-print`) of your file. This enables others to verify the existence, authenticity and (optionally) the ownership of this file/asset.

* _Close the Trust-loop_: before you hand over ownership of your assets to others, others can verify your assets with TikTag.

{{< alert >}}
Q: But we have [IPFS](https://ipfs.io/). It seems to be doing the same jobs as TikTag.

A: Please compare how many steps you need to do the same jobs with your digital assets/files between TikTag and an IPFS-enabled app, not to mention the risks of trusting your NFT-worthy assets on those defunct NFT platforms/apps. TikTag COULD be your last resort for you and your customers' relationship, when all else failed.

By the way, TikTag plans to support IPFS storage as well.
{{< /alert >}}


## How TikTag works

TikTag is firstly shipped as a command line app written in Go, run and used locally.

As you're using TikTag, overtime, your photos' meta data, such as hash, `ttid` (for public sharing), etc, are being logged anonymously on [tiktag.us](https://tiktag.us).

In v1.x, you'll be able to verify the existence, authenticity, integrity and ownership after you've login TikTag with your crypto wallet.

TikTag adds more transparency to how you're keeping your digital assets.

### Globally Unique Asset ID
When you run `tiktag myfile.png`, we assign a globally unique ID to your asset, while you decide where to store them. This user friendly ID will enables easier sharing with others.

### You Keep Your Asset
You store image/asset locally or on cloud storage of your choice, until you feel right to mint their NFT.  [Tiktag.us](https://tiktag.us) DOES NOT host any user assets.

### Opt-in Track & Traceability
You decide how much you want others to know about your asset’s meta info, such as time created or minted and how.

## How TikTag handles privacy?
As a dApp, TikTag handles privacy well by design,

1. You only share meta data of your digital assets handling anonymously to [tiktag.us](https://tiktag.us).
2. You choose which assets to associate with your crypto wallet ID
3. You host your own assets, either on traditional object storage, IPFS, or on any crypto networks


## What next?

Please join the conversation with the [community on Keybase](https://keybase.io/team/tiktagus).

* [Quick Start](/docs/quick-start/): get-started  guide for the impatient master of command line apps
* [How-to](/docs/how-to/): the how-to for different tasks you can handle with TikTag

