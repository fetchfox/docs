# 👨‍🔬 Scraping Candidates From LinkedIn

You can use [FetchFox](https://fetchfoxai.com) to scrape candidates from LinkedIn.

Let's see how to do it, step-by-step.

## Get the extension

If you haven't already, make sure you have the FetchFox extension installed. You can get it from the [Chrome Extension store](https://chromewebstore.google.com/detail/fetchfox/meieeikgpmlhmfjmjgciiclgmbcocfnk?authuser=0\&hl=en).

Follow the setup instructions in the extension, and check [Getting Started](../getting-started.md) for more details if you need it.

## Do a search on LinkedIn

Now that you have the extension, lets go to LinkedIn and get started.

Visit [https://www.linkedin.com/](https://www.linkedin.com/feed/), and find the search bar. Type in the type of job candidates you want to find, for example "Google Engineers," and press Enter.

<figure><img src="../.gitbook/assets/Screenshot 2024-09-25 at 2.04.57 PM.png" alt="" width="563"><figcaption><p>Start by doing a search on LinkedIn</p></figcaption></figure>

On the results page, click the button for "People" to see the candidates you want to search.

<figure><img src="../.gitbook/assets/Screenshot 2024-09-25 at 2.06.57 PM.png" alt="" width="563"><figcaption><p>On the initial results page, click "People"</p></figcaption></figure>

Now it's time to start FetchFox. Click the extensio icon, and type in a prompt describing what you are looking for. You can copy and paste the one below to get started, and change it as you see fit.

> Find candidates, and get the following information:
>
> * ﻿﻿Their current job title
> * ﻿﻿Their current location
> * ﻿﻿Their previous company
> * ﻿﻿Their previous job title
> * ﻿﻿Their university and degree, if any

The more detail, the better.

<figure><img src="../.gitbook/assets/Screenshot 2024-09-25 at 2.10.34 PM.png" alt="" width="563"><figcaption><p>Tell FetchFox what you want to scrape</p></figcaption></figure>

Next, click the little arrow icon in the prompt field. This will use AI to generate a detailed scraping job. You should get something like the screenshot below.

<figure><img src="../.gitbook/assets/Screenshot 2024-09-25 at 2.16.37 PM.png" alt="" width="563"><figcaption><p>Review the scrape fields and click "Run Scrape"</p></figcaption></figure>

When you click "Run Scrape," FetchFox will start by finding links related to your scrape. In this case, it will find links to job candidates. Then, it will visit each page and extract the information you asked for. The progress bar will show how far along the scraper is.

<figure><img src="../.gitbook/assets/Screenshot 2024-09-25 at 2.15.32 PM.png" alt="" width="563"><figcaption><p>The progress bar is an estimate of how much work is left</p></figcaption></figure>

And that's it! Now, just wait.

Once FetchFox finishes, you can download the results as a CSV, or export them to a shareable link.

## Scraping multiple pages

LinkedIn gives many pages of results. You can scrape multiple pages. To do this, scroll to the bottom of the page, find the pagination bar, and click "Next".

<figure><img src="../.gitbook/assets/Screenshot 2024-09-25 at 2.22.59 PM.png" alt="" width="563"><figcaption><p>Go to the next page of results</p></figcaption></figure>

Then, open up FetchFox again, and click "Run Scrape" just like before. FetchFox run the same scrape on the new page, and add the results to what you already have. Repeat as many time as you need.

_**Insider Tip:** We are working on handling pagination automatically, so you don't have to click Next page a hundred times. For updates on this,_ [_Join our Discord_](https://discord.gg/mM54bwdu59)_. If this feature is important to you, message us on there and we'll keep you posted on new releases._
