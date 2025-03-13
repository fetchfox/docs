---
icon: '1'
---

# Single Page / Single Item

The simplest scraper setup is to scrape a single page for a single item.

For example, you might want to get the thread title, thread author, upvotes, and number of comments from a single thread on r/NBA. You'll give the URL of one thread, and get one row of data.

To get started, use the prompt below. It gives the URL you want to scrape, and the data you want from that URL.

<figure><img src="../../.gitbook/assets/Run scrape single page singpe result.png" alt=""><figcaption></figcaption></figure>

On the next page, click on the pencil icon in the “Extract data” section to edit it.

<figure><img src="../../.gitbook/assets/Change to Single Page - Edit.png" alt=""><figcaption></figcaption></figure>

Then change the field “Items per Page” to “Single”.

<figure><img src="../../.gitbook/assets/Choose Single Item - Save.png" alt=""><figcaption></figcaption></figure>

Now click “Save” and click “Run”.

<figure><img src="../../.gitbook/assets/Single Page Save and Run.png" alt=""><figcaption></figcaption></figure>

Your result will be exactly one output, the details about the thread.

<figure><img src="../../.gitbook/assets/Results for Single Page.png" alt=""><figcaption></figcaption></figure>

_Note_: The first step “Results for Starting URLs” does not count as a billable item. But step 2 counts as 1 item and is billable.

What if you have multiple thread links and want to scrape one output per page?

<figure><img src="../../.gitbook/assets/4 Individual pages.png" alt=""><figcaption></figcaption></figure>

You can put in 4 starting URLs, and you will get exactly 4 output items.

<figure><img src="../../.gitbook/assets/4 Items results.png" alt=""><figcaption></figcaption></figure>

However, copy and pasting multiple URLs is a lot of manual work. We don't recommend doing this often. Instead, lets see how we can have FetchFox automatically find all the URLs for us.
