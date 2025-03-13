---
icon: '3'
---

# Multiple Pages / Single Item per Page

_Explanation_: Retrieve one item from multiple pages. For example, let’s say you want the top comment with the most upvotes for each thread. Below is how you can do it with the subreddit /r/SaaS.

From the previous topic, we added a field called ‘url’. This has a special meaning which means when we add a new step, it will scrape those URLs.

<figure><img src="../../.gitbook/assets/url field special meaning.png" alt=""><figcaption></figcaption></figure>

Next, we need to add a new step called “Extract”. First, click the “+” icon (Add Step) after Step 2 (“Extract data”).

<figure><img src="../../.gitbook/assets/add third step multiple pages.png" alt=""><figcaption></figcaption></figure>

Then choose “Extract”.

<figure><img src="../../.gitbook/assets/third step extract data.png" alt=""><figcaption></figcaption></figure>

Now add a field called “top\_comment” with a prompt “Find the top comment of each thread”. The next step is important because we only want the **top comment**, so let’s change the “Items per page” field to “Find exactly one item per page”.

<figure><img src="../../.gitbook/assets/top comments new field and single item.png" alt=""><figcaption></figcaption></figure>

Voila! Now you have a new column with the top comment for each thread page.

<figure><img src="../../.gitbook/assets/reddit SAAS comments 3 steps final.png" alt=""><figcaption></figcaption></figure>

_Note_: This scraped data is from two different “types” of pages. Some of the data is from the top level (i.e. r/SaaS page) and the top comment data is the next level down.
