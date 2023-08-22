---
title: "Version 0.x Design"
linkTitle: "Version 0.x Design"
date: 2022-11-22
weight: 31
description: >
  TikTag v0.x focuses on use-cases validation and early users.
---

TikTag v0.x series offer the following features,

1. Host a photo on storage of user’s choice, and get its URL back as a response,
    - so that you can embed the URL in Markdown editor (of a blogging app) for publishing
    - or simply share the URL with others

2. Generate images in poster format with `tiktag poster`,
    - so that the generated poster can be easily shared on social networks via QR scan,
    - by default, the QR points to your hosted image’s URI such as https://s3.tikoly.com/village/563583552944996352.png, meaning the pointer QR refers to where your image poster is hosted;
Hosted version will support configurable QR, so that it points to your landing page or online object of your own interest.

3. Configure tiktag in ~/.tiktag/config.yml, so that you can decide,
    - which S3 compatible object storage service to host the photo, and
    - which landing URL to generate QR for with `titkag poster` feature.

> Hosted version will support configurable QR, so that it points to your landing page or online object of your own interest.

4. Configure `tiktag` params in `config.yml`, so that you can decide,
    * which S3 compatible object storage service to host the photo,
    * how to search and retrieve a stored asset, by original file (default) and `ttid`,
    * ~~define supported file extention, i.e., png, jpg, etc.~~ (deferred to later versions).

## What's Next?

> If you like the idea of `tiktag` and wish to use it, [let us know what you think](https://github.com/tiktagus/tiktag/issues), or [talk to our developers](https://join.slack.com/t/tiktag/shared_invite/zt-1kdvg6uwx-xruL~AMhYGgd0QezP66~PA).