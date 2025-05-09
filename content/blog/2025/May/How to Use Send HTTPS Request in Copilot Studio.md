---
title: How to Use Send HTTPS Request in Copilot Studio
date: 2025-05-08
tags:
  - HTTPSRequest
  - CopilotStudio
  - APIIntegration
  - LowCode
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
  image: Images/blog_images/2025/May/SendHTTPsinCS.png
  alt: Image for How to Use Send HTTPS Request in Microsoft Copilot Studio
  relative: true
  caption: Generated using [OG Image Playground by Vercel](https://og-playground.vercel.app/)
  hidden: false
---

Microsoft [Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-what-is-copilot-studio) is getting better every day! One of the coolest features is the ability to build your own custom agents with knowledge bases, topics, actions, and channels.

In this blog, I’ll show you how to use the [**Send HTTPS Request**](https://learn.microsoft.com/en-us/microsoft-copilot-studio/authoring-http-node) feature effectively. We’ll create a simple agent that fetches random quotes from the [_Breaking Bad_ API](https://breakingbadquotes.xyz/) (I just love using this API to show examples). The API response will return a quote along with the author’s name (character name) from the series. 

Follow the steps below.

## Step 1: Create a New Agent

Go to [Copilot Studio](https://copilotstudio.microsoft.com) and click on the **New agent** button. For this example, we’ll create the agent **from scratch**, without any use of AI.

![Send Https Request Image 1](/Images/blog_images/2025/May/CS1.png)

Click **Create**.

![Send Https Request Image 2](/Images/blog_images/2025/May/CS2.png)

## Step 2: Add a Topic

You’re inside your brand-new agent! Let's add a new topic. This is where we’ll place our HTTP request logic.

>Topics are like conversation flows. They define how your agent responds in different scenarios.

Create a **manual topic (From blank)** for this demo.

![Send Https Request Image 3](/Images/blog_images/2025/May/CS3.png)

By default, you’ll see some system generated and custom topics.

## Step 3: Add Trigger Phrases

Now, you’ll see a **trigger** created. This is where you define phrases or description that will start the topic.

Enter the following two phrases:

- Give me a breaking bad quote
    
- New quote

![Send Https Request Image 4](/Images/blog_images/2025/May/CS4.png)
## Step 4: Send an HTTPS Request

Click the **+ icon**, choose **Advanced**, and then select **Send an HTTPS Request**.

![Send Https Request Image 5](/Images/blog_images/2025/May/CS5.png)
We’re going to call an open-source API to get quotes from _Breaking Bad_.

Enter this URL:
`https://api.breakingbadquotes.xyz/v1/quotes`

Set the **method** to `GET`.

Also:

- Set the **response type** to `any`
    
- Create a variable (I called mine `Quote`) to store the response
    

This API returns a quote and author, we’ll grab and display only **quote**.

![Send Https Request Image 6](/Images/blog_images/2025/May/CS6.png)

## Step 5: Send the Quote to the User

Let’s show the result to the user. Add a **Send a message** node.

![Send Https Request Image 7](/Images/blog_images/2025/May/CS7.png)
In the message box, use the following `Power Fx` formula to get the quote text:

`First(Topic.Quote).quote`

This pulls the first item from the response and shows the quote.

![Send Https Request Image 8](/Images/blog_images/2025/May/CS8.png)

## Final Step: Name, Save & Test

Give your topic a name like **Get Quote**, then click **Save**. Your topic flow should look something like this:

![Send Https Request Image 9](/Images/blog_images/2025/May/CS9.png)
Now, click **Test**, type **"Give me a breaking bad quote"**, and your agent will fetch a quote from the API and show it!

![Send Https Request Image 10](/Images/blog_images/2025/May/CS10.png)
We just used the **GET** method here, but Copilot Studio also supports **POST**, **PUT**, and **DELETE**.

Share your thoughts below!

Happy building!🐱