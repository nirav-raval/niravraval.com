---
title: Conditional Mapping in ShareGate Using PnP PowerShell
date: 2025-04-11
tags:
  - ShareGate
  - Migration
  - Powershell
  - Metadata-mapping
author: Nirav Raval
showToc: true
TocOpen: true
draft: false
hidemeta: false
comments: true
description: 
canonicalURL: 
disableHLJS: false
disableShare: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
  image: Images/blog_images/2025/April/ShareGatecoverimagePnP.png
  alt: Image for Conditional Mapping in ShareGate Using PnP PowerShell
  relative: true
  caption: Generated using [OG Image Playground by Vercel](https://og-playground.vercel.app/)
  hidden: false
---

In my last [blog post](https://niravraval.com/blog/2025/april/how-to-achieve-conditional-mapping-with-sharegate/#option-2-use-pnp-powershell-after-migration), I explained two ways to tackle conditional mapping in ShareGate. In this post, I'll show you how to use the [PnP PowerShell module]((https://pnp.github.io/powershell/index.html)) to handle conditional mapping more efficiently.

As I mentioned earlier, it's not practical to rely on the ShareGate user interface for each site. That’s where I recommend a better approach -> using PnP PowerShell module.

## PnP PowerShell Script:

No big deal! Here's the scenario I mentioned earlier: you want to run a script that checks each item’s **Status** (a choice column in your SharePoint list), and if it’s set to **“Pending”**, the script should update it to **“Approved”**.

>**Tip:** By default, ShareGate uses PowerShell **v5.0**, but **PnP requires PowerShell v7** to run any scripts. So, if you want to run the PnP module from the same shell, use the `pwsh` command to launch the script.

As of now, this kind of conditional check from source and update it to destination isn’t possible using ShareGate alone.

 {{< gist nirav-raval d0ceaec2e5292b12d3939f63d36c3adf >}} 

>Don’t know your client ID?, As of September 9th, 2024, this has become mandatory step. This[ article](https://pnp.github.io/powershell/articles/registerapplication.html) will guide you through how to do so.

This was just a simple use case. Yours might be more advanced. All the best tackling it! 

Feel free to drop your thoughts or questions in the comments section below, I’d love to help if you're trying something similar.

Thanks again for reading. I hope you're finding these posts helpful.