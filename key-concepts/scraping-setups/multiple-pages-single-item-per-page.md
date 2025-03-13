---
icon: '3'
---

# Multiple Pages / Single Item per Page

This scraper setup gets goes to many different pages, and gets a single item from each one.

For example, let’s say you are scraping comment threads on a Reddit page like https://www.reddit.com/r/SaaS, and you want to get the text of the top comment on each thread. The comment text is not available on the main page, so FetchFox needs to visit the individual pages to get that data.

Let's start with a prompt that tells FetchFox to do this. Try the one below:

> https://www.reddit.com/r/SaaS
>
> Find the URL of each comment thread on this page, and then on each thread page get the author and text of the top comment.  Extract only the top comment.

FetchFox will generate a scraper like this:

<figure><img src="../../.gitbook/assets/many_pages_one_item1_2.png" alt=""><figcaption></figcaption></figure>

This scraper starts on https://www.reddit.com/r/SaaS, and then visit each comment thread, as shown in the diagram below.

<figure><img src="../../.gitbook/assets/crawl_diagram2.png" alt=""><figcaption></figcaption></figure>

A single starting page goes to multiple thread pages. The results are shown below:

<figure><img src="../../.gitbook/assets/many_results2.png" alt=""><figcaption></figcaption></figure>

As you can see, FetchFox collected data from each comment thread.

_Note_: This scraped data is from two different “types” of pages. Some of the data is from the top level (i.e. r/SaaS page) and the top comment data is the next level down.
