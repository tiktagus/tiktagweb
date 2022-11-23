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

When you're using `tiktag` locally on a daily basis, you're leaving an audit trail with [tiktag.us](https://tiktag.us), including the file's fingerprint, time of operation, etc. For example, when you first hosted a file, we got its `ttid` as part of the URL, and the timestamp.

Once you login [tiktag.us](https://tiktag.us) with your wallet, you'll need to go through a simple proof-of-ownership test. We'll implement Zero Knowledge algorithm to verify your claim on the asset's ownership, leaving a proof for others to check and verify.

This is happening on an on-going basis as you keep using `tiktag` with a wallet you are controlling. Over time, `tiktag` makes it easier for you to prove your relationship with the asset in question.

## What's Next?

> If you like the idea of `tiktag` and wish to use it, [let us know what you think](https://github.com/tikoly-com/tiktag/issues), or [talk to our developers](https://join.slack.com/t/tiktag/shared_invite/zt-1kdvg6uwx-xruL~AMhYGgd0QezP66~PA).