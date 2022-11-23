---
title: "Version 1.x Design"
linkTitle: "Version 1.x Design"
date: 2022-11-23
description: >
  TikTag v1.x focuses on asset ownership with wallet login.
---

> You guessed right. We're not tackling any _ownership_ features in v0.x, with good reasons.

## Ownership is Verified on Wallet Login

You created a digital file, image or photo, locally on your PC. There is nothing special on proof-of-ownership other than the fact that you've created something meaningful only to yourself (or your team).

Once you've logged in with wallet on [tiktag.us](https://tiktag.us) (when we reach v1.0), you'll need to perform a few local `tiktag` command to verify to `tiktag.us` that you own certain set of files, like,

```
> tiktag -v [my wallet's public key]
```

Or, we may implement a web GUI feature to verify that you, the wallet owner, is actually owner of the digital assets you've `tiktag`-ed previously.

## How Does It works

When you're using `tiktag` locally on a daily basis, you're leaving an audit trail with [tiktag.us](https://tiktag.us), i.e., the file's unique ID, digital fingerprint, timestamp of your operation, etc. We'll implement a Zero Knowledge algorithm to verify that you are owning the assets, and leaving a proof for others to check and verify when necessary.

This is an on-going basis as you keep using `tiktag` with a bineded wallet you are controlling. This way, we're capable of proving to the world that you own what you've claimed to own.

## What's Next?

> If you like the idea of `tiktag` and wish to use it, [let us know what you think](https://github.com/tikoly-com/tiktag/issues), or [talk to our developers](https://join.slack.com/t/tiktag/shared_invite/zt-1kdvg6uwx-xruL~AMhYGgd0QezP66~PA).