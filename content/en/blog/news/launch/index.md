---
date: 2022-11-22
title: "Why we need to audit digital asset"
linkTitle: "Annoucing TikTag"
description: "TikTag is a tool to make the handling of digital asset, such as photo, _auditable_."
author: Chance Jiang ([@chancejiang](https://twitter.com/chancejiang))
resources:
- src: "**.{png,jpg}"
  title: "Image #:counter"
  params:
    byline: "Photo: Chance Jiang / CC-BY-CA"
---

I admit, we didn't set out to build a tool to make digital asset auditable.

## In the beginning...

I wanted to start a new blog I can edit and publish in Markdown. I want to regularly post photos in my blog posts. This requires me to,

1. prepare the image, store it somewhere such as a [MinIO](https://min.io/) instance;
2. get the URL from the the image I just stored;
3. embed the URL in my blog post.

The above workflow takes me about 3 minutes. But I felt it annoying to have to repeat it for each image I'm posting. So I imagined a command-line tool that I can use to automate the entire process. Out of my product manager's weird habbit of naming things, I even thought of a name for the command, `TikTag`.

And I imagined I could use `tiktag` like this,
 ```
> tiktag myfilename.png
> Tik...success! Tag...your asset is hosted at,
> https://s3.tikoly.com/village/563583552944996352.png
```
So, once you're done `tiktag`-ing your photo, you'll get something like, `https://s3.tikoly.com/village/563583552944996352.png`.

Neat.

Then, in your Markdown editor, you can embed your photo like,
```
![my image](https://s3.tikoly.com/village/563583552944996352.png)
```
which renders to,
![myfile.png](https://s3.tikoly.com/village/563583552944996352.png)

This image editing workflow feels _neat_, doesn't it? We think so, too.

> That's why we decided to build `tiktag`, initally.

## Then, we had more ideas for `tiktag`

I was tasked to come up with an open source tool for photo editors who're looking forward to easy tooling for minting NFT.

{{< imgproc ship Fill "640x640" >}}
Fetch and scale an image in the upcoming Hugo 0.43.
{{< /imgproc >}}

The front matter of this post specifies properties to be assigned to all image resources:

```
resources:
- src: "**.{png,jpg}"
  title: "Image #:counter"
  params:
    byline: "Photo: Chance Jiang / CC-BY-CA"
```

## Here we are, _soft launching_ TikTag

Even it's a WIP - Work in Progress, and even it's a design blueprint to be coded and shipped, since we believe in the *Build in Public* open source culture, we decided to launch `tiktag` as soon as possible.

Stay tuned and let's explore more possibilities with **TikTag** together!

## What's next?

* Learn more about our product design for [TikTag v0.x](/blog/20221123/version-0.x-design/) and [TikTag v1.x](/blog/20221123/version-1.x-design/).

* If you like the idea of `tiktag` and wish to use it, [let us know what you think](https://github.com/tikoly-com/tiktag/issues), or [talk to our developers](https://join.slack.com/t/tiktag/shared_invite/zt-1kdvg6uwx-xruL~AMhYGgd0QezP66~PA).

