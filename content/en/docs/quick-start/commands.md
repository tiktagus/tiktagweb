---
categories: ["quick-start"]
tags: ["commands", "quick-start", "docs"]
title: "Commands"
linkTitle: "List of Commands"
draft: false
date: 2022-12-22
description: >
  Complete list of `tiktag`
---

{{% pageinfo %}}
Work in progress, NOT all are implemented.
{{% /pageinfo %}}

----------------

Complete list of command, sub-commands and options for using `tiktag` CLI.

## `tiktag`

The entry command for `tiktag` CLI.

### Synopsis

`tiktag` is the main command, used to host and share your assets.

```Shell
> tiktag myfilename.png
> Tik ...Tag ... your asset is successfully hosted at,
> https://s3.tikoly.com/village/563583552944996352.png
```

### Sub-commands and Options

```shell
-f, --find    string    search for an asset/image, i.e., `tiktag -f my_file_name.png`
-s, --sync <null>    manually synchronize or upload all assets onto (new) object storage
```