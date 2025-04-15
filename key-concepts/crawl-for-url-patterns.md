---
icon: sparkles
---

# Crawl for URL patterns

You can use FetchFox to crawl a website for a URL pattern.

A URL pattern starts with "http", and includes at least one wildcard "\*" charcters.

Here is an example:

```
https://www.example.com/category/*
```

This URL pattern would match all of these URLs:

```
https://www.example.com/category/page-1
https://www.example.com/category/page-2
https://www.example.com/category/sub-cat-a
https://www.example.com/category/sub-cat-a/some-article
https://www.example.com/category/helpdesk?question_id=111
```

You can include multiple wildcards to match specific patterns, like this:

```
https://www.example.com/category/*/items/*
```

This URL pattern will match all of these URLs:

```
https://www.example.com/category/toys/items/11
https://www.example.com/category/toys/items/22
https://www.example.com/category/toys/items/33
https://www.example.com/category/books/items/111
https://www.example.com/category/books/items/222
https://www.example.com/category/books/items/333
```

## Why use URL patterns?

It is useful to crawl for URL patterns if you want to find many pages that have similar data. Web sites use URLs to organize their data, and you can use that organization in your scraper.

For example, if you are scraping e-commerce data, you may notice that all the products have a URLs like this:

```
https://www.some-store.com/shop/products/111-basic-soap
https://www.some-store.com/shop/products/222-fancy-soap
...and so on...
```

A URL pattern is an easy way to find all the products. Just put in "\*" for the part that changes

```
https://www.some-store.com/shop/products/*
```

## Scraping Pokemon Moves with URL patterns

Lets do an example scrape using URL patterns. We're going to scrape all the Pokemon moves using URL patterns.

You can find Pokemon moves at URLs like this:

* [https://pokemondb.net/move/growl](https://pokemondb.net/move/growl)
* [https://pokemondb.net/move/scratch](https://pokemondb.net/move/scratch)
* [https://pokemondb.net/move/ember](https://pokemondb.net/move/ember)
* ...and so on...

You'll notice they all have this format:

```
https://pokemondb.net/move/*
```

This format becomes our URL pattern. Let's get started.

As a first step, make a new scrape at [https://fetchfox.ai/new](https://fetchfox.ai/new), and put in the top level URL of the site, like this:

<figure><img src="../.gitbook/assets/CleanShot 2025-04-15 at 14.45.37@2x.png" alt=""><figcaption><p>Put in any URL from the target site to get started</p></figcaption></figure>

Click the arrow to continue, and wait for FetchFox to initialize your workflow.

For this scrape, remove any steps that FetchFox created so we have a blank workflow.

<figure><img src="../.gitbook/assets/CleanShot 2025-04-15 at 14.51.41@2x.png" alt=""><figcaption><p>Create a blank workflow by removing any steps FetchFox added</p></figcaption></figure>

Then, add a "Crawl" step by clicking the plus icon.

<figure><img src="../.gitbook/assets/CleanShot 2025-04-15 at 14.51.49@2x.png" alt=""><figcaption><p>Add a "Crawl" step</p></figcaption></figure>

Then, select the option to crawl based on a URL pattern:

<figure><img src="../.gitbook/assets/CleanShot 2025-04-15 at 14.53.31@2x.png" alt=""><figcaption><p>Use the option that crawls for URL patterns</p></figcaption></figure>

Enter the URL pattern from before, which is

```
https://pokemondb.net/move/*
```

And then click "Save".

<figure><img src="../.gitbook/assets/CleanShot 2025-04-15 at 14.55.15@2x.png" alt=""><figcaption><p>Enter your URL pattern for the crawl.</p></figcaption></figure>

For URL pattern crawls, make sure to put in a limit on the number of results. These often find many results, and if you don't put in a limit, you will [quickly burn through your credits](pricing.md).

<figure><img src="../.gitbook/assets/CleanShot 2025-04-15 at 15.00.19@2x.png" alt=""><figcaption><p>Put in a limit for the crawl</p></figcaption></figure>

Click "Run", and you should see results like the screenshot below.

<figure><img src="../.gitbook/assets/CleanShot 2025-04-15 at 15.02.11@2x (1).png" alt=""><figcaption><p>Results for the URL pattern crawl.</p></figcaption></figure>

We can combine this with extraction to get data out of each page. To do this, add an extract step using the plus icon.

<figure><img src="../.gitbook/assets/CleanShot 2025-04-15 at 15.04.39@2x.png" alt=""><figcaption><p>You can extract data from the pages you found.</p></figcaption></figure>

For this example, add the following fields:

> name: Move name
>
> type: Move type
>
> power: Move power

Make sure to tell the AI to scrape a single item per page, and click save.

Run the scraper again. Your results should look something like this:

<figure><img src="../.gitbook/assets/CleanShot 2025-04-15 at 15.11.24@2x.png" alt=""><figcaption><p>Extraction can follow a crawl step</p></figcaption></figure>

Combining a URL pattern crawl and a data extraction step is an easy and powerful way to scrape data from many websites.
