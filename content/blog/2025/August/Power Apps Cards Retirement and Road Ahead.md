---
title: Power Apps Cards Retirement and Road Ahead
date: 2025-08-15
tags:
  - PowerApps
  - AdaptiveCards
  - MicrosoftTeams
  - OutlookActionableMessages
author: Nirav Raval
showToc: true
TocOpen: false
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
  image: Images/blog_images/2025/August/test.png
  alt: Image for PowerApps Card Deprecation
  relative: true
  caption: 
  hidden: false
---

If you’ve been using Cards for Power Apps in Teams, kindly note that they will be [deprecated](https://learn.microsoft.com/en-us/power-platform/important-changes-coming#deprecation-of-cards-for-power-apps) on **August 29, 2025**. However, there are few alternatives available, and in this blog post, I will guide you through those.
## What's Happening?

After August 29, 2025, three major things happen:

- Existing PowerApps cards in Teams will stop working.
- You can’t create new ones.   
- Any flows or automations that rely on them will break.

Microsoft is moving everything to Adaptive Cards, which are now seen as the standard format across Teams, Outlook, and your favorite Copilot.
## What is Adaptive Cards ?

If you’re not familiar, [Adaptive Cards](https://adaptivecards.io/) are basically rich, interactive UI snippets described in JSON. You can use them to collect inputs, display dynamic information, trigger actions, or even handle approvals. For example, a help desk ticket card can display fields such as "Title" and "Description," along with a submit button, allowing users to send this information directly to Power Automate without leaving Teams or Outlook.

![PowerApps Cards Deprication Image 1](/Images/blog_images/2025/August/AC_1.png)

Few advantages that I can think for Adaptive cards...

- Adapt to the app they’re in (Teams, Outlook, Windows, etc.).
- Support text, images, buttons, and input fields.
- Look native in light/dark mode.
- Work in multiple places without rebuilding.

In short, it's piece of a card with one design, but can work on many platforms.

## Which option should you select?

Below are three recommendations you can choose from based on your goals.

1. **Adaptive cards in Teams** - You can deliver these without coding using **Power Automate**. Create the card in JSON, post it to a chat or channel, and collect responses directly in Teams. Perfect for quick updates, collecting feedback, or handling approvals. Bots can also send these cards for more dynamic scenarios.

![PowerApps Cards Deprication Image 2](/Images/blog_images/2025/August/AC_2.png)

2. **Adaptive cards in Copilot Studio** - If you’re building in Copilot Studio, you can present Adaptive Cards right in a conversation. For example, when a user says "Log a help desk ticket", Copilot can show a card asking for details, then trigger your automation once submitted — all inside the chat.

![PowerApps Cards Deprication Image 3](/Images/blog_images/2025/August/AC_3.png)

3. **Outlook Actionable Messages** - These are Adaptive Cards embedded in Outlook emails. The recipient can approve, reject, or submit information without leaving their inbox.

![PowerApps Cards Deprication Image 4](/Images/blog_images/2025/August/AC_4.png)

## My View

Accept it and move on! You don’t have to stop using Power Apps. But make sure instead of putting the card inside Power Apps, you switch it in Teams, Outlook, or Copilot, then send the responses back to your Power Apps app or Dataverse tables. This way, your backend stays the same, but the front-end experience becomes more modern and works across more places.

I know it’s a tedious task and will take some effort now, but once you’ve moved to Adaptive Cards, your solutions will look cleaner, and with Microsoft backing it you can trust it’s here to stay. You know what I mean! 😉

**Useful Resources**

* [Power Apps cards overview](https://learn.microsoft.com/en-us/power-apps/cards/overview)
* [Adaptive cards in Power Automate](https://learn.microsoft.com/en-us/power-automate/overview-adaptive-cards)
* ["Ask with Adaptive Card" in Microsoft Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-ask-with-adaptive-card)
* [Actionable messages in Outlook](https://learn.microsoft.com/en-us/outlook/actionable-messages/)

