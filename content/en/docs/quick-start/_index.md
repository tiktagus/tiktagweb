---
categories: ["quick-start"]
tags: ["how-to","docs"] 
title: "Quick Start"
linkTitle: "Quick Start"
weight: 2
description: >
  Get-started guide for the impatient master of command line app
---

{{% pageinfo %}}
Make sure you already have [Golang](https://go.dev/doc/install) install on your PC.
{{% /pageinfo %}}

## Install TikTag
{{< alert >}}
Suppose you've openned your command line console app and you know where your photo/asset files directory is. For MacOS users, press `Apple key + Space`, when promoted, type `Terminal` and press `Enter`.
{{< /alert >}}

### `go install` tiktag
Go to your working directory of photos/assets,
```Shell
> cd /directory/to/my-photo-directory
```

then install `tiktag` by running the following command,
```Shell
> go install github.com/tiktagus/tiktag@latest
```

### Configure `tiktag`
Once TikTag is installed, you shall see `config.yml` on your project's directory root. But it's not yet ready for use. You need to configure at lease ONE object storage service, such as with the following params,

```yaml
# TikTag Configuration
defaultStorage: $My-Mino-Instance
title: My TikTag

storage:
  name: My-Mino-Instance
    targetURL: my-minio-service-URL // replace this, with such as `https://s3.tikoly.com`
    accessKey: super-secret-string // replace this
    secretKey: super-secret-key-string // replace this
    targetBucket: name-of-bucket // replace this
  name: My-AWS-S3-Instance
  ...
```

## Host an asset (v0.x)

```Shell
tiktag myfilename.png
Tik ...Tag ... your asset is successfully hosted at,
https://s3.tikoly.com/village/563583552944996352.png
```

## Retrieve an asset's URI (v0.x)

```Shell
> tiktag search myfilename.png
> We found this asset at,
> https://s3.tikoly.com/village/563583552944996352.png
```
{{< alert >}}
This command depends on 
You can also use this command to check if an asset has been hosted or not.
{{< /alert >}}

## Track an asset's ownership (v1.x)
This is a planned feature for v1.x, when web GUI is ready on [tiktag.us](https://tiktag.us).

```Shell
> tiktag whose myfilename.png
> We found,
> Sui Wallet https://etherscan.io/address/0x6ce19a00f0424b27bc2fce5ec3f10ba022a42370
> Please visit https://tiktag.us/ for more options.
```

