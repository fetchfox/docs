---
icon: '4'
---

# Multiple Pages / Multiple Items

Explanation: Extract several items from multiple pages. For example, let’s say we want to scrape all the thread titles on r/RealEstate and then scrape all the comments in those threads.

We can insert the starting URL and a prompt such as below.

```https://www.reddit.com/r/realestate/
https://www.reddit.com/r/RealEstate/

find URLs of all the comment threads
```

<figure><img src="../../.gitbook/assets/real estate run scrape.png" alt=""><figcaption></figcaption></figure>

Now we need to remove the second step (Find more URLs) and replace it with the Extract data box. And also edit the third step where we will add new fields.

<figure><img src="../../.gitbook/assets/real estate remove 2nd step edit 3rd step.png" alt=""><figcaption></figcaption></figure>

First, let’s start with the second step.

_Note_: The exact workflow may vary but in our case, let’s delete the current “Find more URLs” box, add a new second step (+ icon), and choose “Extract”.

<figure><img src="../../.gitbook/assets/real estate new 2nd step extract.png" alt=""><figcaption></figcaption></figure>

Now add the following fields below and make sure to change “Items per page” to “Find multiple items per page”. This means that it will scrape all the URL comments from each thread as well as the corresponding thread title.

```
url | URL of the comment thread
thread_title | Find the thread title
```

<figure><img src="../../.gitbook/assets/real estate add 2 fields and multile items save.png" alt=""><figcaption></figcaption></figure>

For the third step, edit the fields and add the following and make sure to once again, choose “Find multiple items per page” so we can extract all the comment texts and authors from the second step:

```
comment_text | What is the text of the comment?
comment_author | Who is the author of the comment?
```

<figure><img src="../../.gitbook/assets/real estate 3rd step 2 fields and multiple items.png" alt=""><figcaption></figcaption></figure>

And there you have it. You just scraped multiple items from multiple pages!

<figure><img src="../../.gitbook/assets/real estate final results.png" alt=""><figcaption></figcaption></figure>

Awesome! Now you’ve learned FetchFox’s scraping setups. 🎉

In the next section, you’ll learn how pagination works.
