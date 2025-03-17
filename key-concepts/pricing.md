# 💵 Pricing

FetchFox charges a flat price of $1 per 1000 items scraped.

A item scraped is an output from a webpage. Depending on your [scraper setup](scraping-setups/), a single page may give one item, or multiple items.

The app will show the number of items scraped in the results area. For example, the scraper below has 2 items scraped.

<figure><img src="../.gitbook/assets/Screenshot 2025-03-17 at 3.31.00 PM.png" alt=""><figcaption><p>This scraper has two items scraped</p></figcaption></figure>

It is important to note that intermediate steps also count as billable items. For example, the scraper below has two steps which each produce 41 items, for a total of 81 items scraped. The starting point step is _not_ counted as billable items.

<figure><img src="../.gitbook/assets/SCR-20250317-ntts (1).png" alt=""><figcaption><p>These two steps combine for 82 billable items.</p></figcaption></figure>

If you are running a template, each intermediate step in the template counts as a billable item. The FetchFox will show you the number of billable items in each intermediate step. The example above is a template that added a total of 159 billable items. This number is larger than the final output of 100 billable items, because FetchFox had to crawl some intermediate pages to get the end result.

<figure><img src="../.gitbook/assets/Screenshot 2025-03-17 at 3.39.11 PM.png" alt=""><figcaption><p>Templates may add multiple items due to their intermediate steps</p></figcaption></figure>

