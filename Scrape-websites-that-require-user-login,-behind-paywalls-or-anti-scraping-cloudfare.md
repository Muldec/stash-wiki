A regular scraper can only scrape information from webpages that are open to the public access. If you want to scrape a webpage that requires login or behind a paywall, you need to use the "Visible CDP" technique. So far this technique is tested and passed under Windows 10 only. <p>
Normal CDP scraping will launch a headless chrome browser, which will not show up for any user interactions. "Visible CDP" turns the "headless chrome" into a "visible" instance which users can interact with.<p>
Steps: <p>
1. Prepare your scraper .yml file and make sure it's valid and working.
2. Run a command console. Goes to Chrome's binary directory and run `chrome.exe --remote-debugging-port=9222`. This will launch a special Chrome instance that Stash Scrapers can control later on.
3. In Stash, make sure the "Chrome CDP Path" setting is `http://localhost:9222/json/version`.
4. Make sure your scraper has the following:
```
driver:
  useCDP: true
```
5. Use the special Chrome instance you launch earlier, go to the webpage you want to scrape, type in your user/pass or pass any other human test, until you see the page with desired content.
6. Paste the webpage's URL in your Stash scene and start scraping. It should get the information correctly.