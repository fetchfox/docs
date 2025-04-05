---
icon: m
---

# Make.com

You can use Make.com to connect any FetchFox scraper to hundreds of other apps using our [official Make.com app](https://www.make.com/en/integrations/fetchfox).

To get started, log in to your Make.com account, and create a new scenario.

<figure><img src="../.gitbook/assets/CleanShot 2025-04-04 at 21.38.50@2x.png" alt=""><figcaption><p>Create a new scenario</p></figcaption></figure>

In your new scenario, FetchFox will be the first step. Click the big "+" sign to add a step, and select "Watch for Scraped Data."

<figure><img src="../.gitbook/assets/CleanShot 2025-04-04 at 21.40.33@2x.png" alt=""><figcaption><p>Add FetchFox as the first step</p></figcaption></figure>

The first time you set up an integration, you'll need to connect your FetchFox account. You do this using your API key, which is available on your account settings at [https://fetchfox.ai/settings](https://fetchfox.ai/settings). It starts with "ff\_".

<figure><img src="../.gitbook/assets/CleanShot 2025-04-04 at 21.43.53@2x.png" alt=""><figcaption></figcaption></figure>



After you add your API key, the integration will pull your existing scrapers. If you don't already have one, read our [quick start tutorial](../getting-started/quickstart-pokemon-edition.md) on how to set up a scraper.

<figure><img src="../.gitbook/assets/CleanShot 2025-04-04 at 21.46.21@2x (1).png" alt=""><figcaption><p>Select the scraper to integrate</p></figcaption></figure>

For the next step, "Choose where to start", pick "All" to bring in all your data, or use one of the other options depending on your preference.

<figure><img src="../.gitbook/assets/CleanShot 2025-04-04 at 21.49.23@2x.png" alt=""><figcaption><p>Bring in all your data with the "All" option</p></figcaption></figure>

After clicking save, do a test run to see if it's working. Click "Run once" in the bottom toolbar.

<figure><img src="../.gitbook/assets/CleanShot 2025-04-04 at 22.09.21@2x.png" alt=""><figcaption><p>Do a test run of the integration</p></figcaption></figure>

If it worked correctly, you can inspect the results and see various output bundles from FetchFox.

<figure><img src="../.gitbook/assets/CleanShot 2025-04-04 at 22.08.37@2x.png" alt=""><figcaption><p>Each bundle is one scraped item from FetchFox</p></figcaption></figure>

Once you've confirmed that FetchFox is sending results to Make.com, you can add the next step of your automation. For example, you can connect FetchFox to Google Sheets. To start, add Google Sheets as the next step, and select "Add a Row".

<figure><img src="../.gitbook/assets/CleanShot 2025-04-04 at 22.14.53@2x.png" alt=""><figcaption><p>You can add a row to Google Sheets</p></figcaption></figure>

Then, configure the connection to Google Sheets by picking a spreadsheet and a sheet within that spreadsheet.

<figure><img src="../.gitbook/assets/CleanShot 2025-04-04 at 22.15.25@2x.png" alt=""><figcaption><p>Set up the Google Sheets connection</p></figcaption></figure>

Finally, map the scraped items to columns in Google Sheets.

<figure><img src="../.gitbook/assets/CleanShot 2025-04-04 at 22.15.41@2x.png" alt=""><figcaption><p>Map scraped data to columns</p></figcaption></figure>

Once you're done, the completed mapping will be look like this.

<figure><img src="../.gitbook/assets/CleanShot 2025-04-04 at 22.15.54@2x.png" alt=""><figcaption><p>Completed mapping between FetchFox and Google Sheets</p></figcaption></figure>

Click "Run once" again to test it, and check your spreadsheet to confirm that the results were updated.

From here, you can add many more integrations using the Make.com ecosystem.
