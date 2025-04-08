---
icon: arrow-progress
---

# n8n

The [n8n](https://n8n.io) app is a powerful workflow automation tool. You can add the [FetchFox node](https://github.com/fetchfox/n8n-nodes-fetchfox) into n8n to integrate AI scraping into your workflows.

In this tutorial, we'll walk through an example of how you can use FetchFox and n8n to do market research on Reddit.

## Installation

Make sure you have the FetchFox n8n node installed. You can follow the n8n instructions on [installing community nodes](https://docs.n8n.io/integrations/community-nodes/installation/) to install the "n8n-nodes-fetchfox" node.

## Start by crawling

For this example, we're going scrape the n8n subreddit, and see what companies people are talking about. Our end goal is a list of company names, and number of times those companies were mentioned.

To do this, we'll first need some comment threads. So lets add the first FetchFox node

<figure><img src=".gitbook/assets/CleanShot 2025-04-08 at 09.52.16@2x.png" alt=""><figcaption><p>Search for the FetchFox node</p></figcaption></figure>

Click on "FetchFox", and then choose "Find pages matching a pattern"

<figure><img src=".gitbook/assets/CleanShot 2025-04-08 at 09.52.27@2x.png" alt=""><figcaption><p>We're going to look for URLs that match a patter</p></figcaption></figure>

The first time you add a FetchFox node, you'll need to add your API key. You can find this a on your settings page at [https://fetchfox.ai/settings](https://fetchfox.ai/settings). Enter it into n8n.

Once you have your credential, you can set up the node to crawl for URLs on Reddit. We're looking for comment threads on r/n8n, and you'll notice that all comment threads have this pattern:

```
https://old.reddit.com/r/n8n/comments/*
```

The "\*" is a wildcard matcher. Put this URL pattern into n8n as shown below.

<figure><img src=".gitbook/assets/CleanShot 2025-04-08 at 10.13.44@2x.png" alt=""><figcaption><p>Find URLs matching a pattern</p></figcaption></figure>

Click "Test Step", and within a few minute, FetchFox will find URLs for some comment threads. It should look something like this:

<figure><img src=".gitbook/assets/CleanShot 2025-04-08 at 10.17.43@2x.png" alt=""><figcaption></figcaption></figure>

Next, lets find out what companies people are talking about. For this, we'll use FetchFox to extract data.

Close the first, and add a new FetchFox node.

This time, add a node to do extraction, and pick "Extract multiple items per URL". This will find all the comments on each comment page.

<figure><img src=".gitbook/assets/CleanShot 2025-04-08 at 10.20.29@2x.png" alt=""><figcaption><p>Use multiple item extraction to get all the data</p></figcaption></figure>

To set up the extraction node, first tell FetchFox which URL to target. Drag the URL field from the previous node into the extraction node.

<figure><img src=".gitbook/assets/CleanShot 2025-04-08 at 10.23.38@2x.png" alt=""><figcaption><p>Use the URLs from the previous node</p></figcaption></figure>

Then, lets add an extraction field. Click the button that says "Add data field to extract", and add one for company.

<figure><img src=".gitbook/assets/CleanShot 2025-04-08 at 10.27.05@2x.png" alt=""><figcaption><p>Tell FetchFox what to extract</p></figcaption></figure>

The entries here will be passed to the AI, so follow prompt writing best practices. The field description below is a good one for this tutorial:

> I am looking for companies being discussed. Give the names of each company discussed in the comments, one by one, in the standard spelling.

When you're done, click "Test Step". You should see something like this:

<figure><img src=".gitbook/assets/CleanShot 2025-04-08 at 10.30.18@2x.png" alt=""><figcaption><p>The results show companies discussed on r/n8n</p></figcaption></figure>

This is a simple two step scraper workflow, and its very common. First, you find URLs, and then you get some data out of them.

We can plug this into a larger n8n workflow. For example, you can add a count and sort node to see the most frequently mentioned companies.

Your final workflow will look something like this:

<figure><img src=".gitbook/assets/CleanShot 2025-04-08 at 10.35.18@2x.png" alt=""><figcaption><p>A full workflow to scrape and summarize data using FetchFox</p></figcaption></figure>

The results in the final node should look something like this:

<figure><img src=".gitbook/assets/CleanShot 2025-04-08 at 10.34.46@2x.png" alt=""><figcaption><p>Final results show the most frequently mentioned companies</p></figcaption></figure>

The FetchFox node is a poweful way to get any data from any website, and integrate it into your n8n workflows.
