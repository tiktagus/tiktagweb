---
title: "Version 0.x Design"
linkTitle: "Version 0.x Design"
date: 2022-11-22
description: >
  `TikTag` v0.x focuses on use case validation, performance, and user feedback.
---

TikTag v0.x series offer the following features,

- Install on user's local machine, and run as a command-line app
- Host a photo on storage of user's choice, and get its URL back as a response
  * so that you can embed the URL in Markdown editor (of a blogging app) for publishing
  * or simply share the URL to others
- Configure `tiktag` params in `config.yml`, so that you can decide,
  * which S3 compatible object storage service to host the photo
  * how to search and retrieve a stored asset, by original file (default) and `ttid`
  * ~~define supported file extention, i.e., png, jpg, etc.~~ (may defer to later versions)

## What's Next?

> If you like the idea of `tiktag` and wish to use it, [let us know what you think](https://github.com/tikoly-com/tiktag/issues), or [talk to our developers](https://join.slack.com/t/tiktag/shared_invite/zt-1kdvg6uwx-xruL~AMhYGgd0QezP66~PA).