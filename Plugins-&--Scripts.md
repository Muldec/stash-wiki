# Plugins
Stash plugins add further features that Stash doesn't itself provide.

To install a plugin, save them to `%USERPROFILE%\.stash\plugins` on Windows or `/root/.stash/plugins` on Unix systems (Mac, Linux, etc.). The `plugins` directory won't exist by default so you will have to create it. Once installed, go to the Plugins page in your Stash settings and reload plugins.

A community-curated repository of scripts and plugins is available here: https://github.com/stashapp/CommunityScripts

### List of Plugins

Category | Plugin | Author | Description
-|-|-|-
Downloader | [YT-DL Downloader](https://github.com/niemands/StashPlugins) | niemands | Download Videos automated with yt-dl and add the scrape tag for burl_url_scraper |
Images | [Gallery Tags](https://github.com/niemands/StashPlugins) | niemands | Copy information from attached scene to galleries   |
Images | [Update Image Titles](https://github.com/niemands/StashPlugins) | niemands | Update all image titles (Fixes natural sort)        |
Maintenance | [Duplicate Finder](https://github.com/WithoutPants/stash-plugin-duplicate-finder) | WithoutPants | Detects and marks duplicate scenes within Stash
Metadata | [Performer Creator](https://github.com/com1234475/stash-plugin-performer-creator) | com1234475 | Creates performers from scenes
Metadata | [Set PH Urls](https://github.com/niemands/StashPlugins) | niemands | Add urls to pornhub scenes downloaded by Youtube-dl |
Scraping | [Bulk URL Scraper](https://github.com/niemands/StashPlugins) | niemands | Bulk scene url scraping                             |
Scraping | [Scrape with](https://github.com/Tweeticoats/stash-plugin-scrape_with)|Tweeticoats | Batch scrape scenes and performers. For example tag a scene with scrape_with_xbvr and run the task to run that scraper. Run artist scrapers on all performers missing a url. Run the performer image scraper on all performers.

# Scripts
Scripts are standalone programs that can interact with stash either through graphql queries or by directly editing stash's database/files.

To install a script follow the script's install instructions.

### List of scripts

Category | Script | Author | Description
-|-|-|-
Maintenance | [SQLITE Renamer for Stash](https://github.com/Belleyy/Stash-Renamer-Python) | Belley  | Renames your files using stash's metadata
