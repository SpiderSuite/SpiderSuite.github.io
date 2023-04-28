---
layout: page
title: Analysis
menubar: docs_menu
show_sidebar: false
toc: true
hero_height: is-small
---

The crawl phase of a scan involves navigating around the target web application, following links and submitting forms to catalog the content of the entire target web application and the navigational paths within it to create an accurate map of the target web application.

## **Configure the crawler**

Next step is to set the configurations for the crawler to run on.

`This is a very crucial step` as the performance and success of the crawler depends on the configurations you have set. Take time to study the effects of all the [Configrations](Configurations).

Click the <img src="/docs/res/config_action.png"  width=14> (`config action`) on the toolbar to get access to the configuration dialog where you can set preferred configurations.

The configurations that affect the crawler are:

- **Limits**- Sets all the limitations for the crawler

- **Crawler**- Sets all the essesntial crawler configurations

- **Headers**- Sets the http request headers to be used by the crawler request.

- **Input Fields**- Sets the values for the page's input fields for automatic filling and submition.

- **Exclusion**- Sets the paths, cookies, file extensions and url parameters to be excluded for the crawl.

- **Authentication**- Sets values for automatic authentication by the crawler.

- **Proxy**- Sets the proxy address and port where all crawl request will pass through.


## **Crawling from a Single Link**
Spider Suite can crawl an entire target web application from a single link which acts as the root entry page for target web application.

To start crawling requires you to follow the following simple and few procedures.

* **Input the target link**

Add the target url link.

<center><img src="/docs/res/filled_input.png"></center>

_**Few things to Note:**_

Always make sure that you have input a valid url with its protocal/schema.
    
    - Valid Links are:
         https://example.com
         https://example.com/
         https://example.com/path1/path2
         https://example.com:443/path1
         https://127.0.0.1:80

    - Invalid Links are:
        example.com
        https://example/
        https://example.com?param1=value1&param2=value2

* **Start Crawler**

Start the crawler by clicking on the `Crawl` button and the crawler with immediately start crawling the target web application.

<center><img src="/docs/res/crawling.png"></center>

After starting the crawler, you can observer the crawler's `progress` on the far right corner which shows the number of pages crawled per all the pages available:

progress = <pages_crawled> / <total_pages>.

After crawler has started you have options to `pause` or `stop` the crawler.

* **Pause Crawler**

Spider Suite allows you to pause the crawler at any point during crawling and for any duration of time by pressing the `Pause` button.

After pressing `Pause` button the crawler immediately pauses sending the requests to the server or processing new replies `but` all the already finished and processed pages will still be added to the sitemap, so its not uncommon to pause the crawler and still seeing a few pages being added to the sitemap.

* **Resume Crawler**

After pausing the crawler you can resume crawling by pressing the `Resume` button and the crawler will immediately resume crawling the target web pages where it left of.

* **Stop Crawler**

You can stop the crawler at any point in time by pressing the `Stop` button. Stopping the crawler means that you terminate the crawler and you can no longer resume that particular crawl, all resources allocated are cleaned hence you can only start afresh from there.

After pressing `Stop` button the crawler immediately stops sending the requests to the server `but` it will wait untill all the already sent request to be processed and added to the sitemap before it kills all the crawler threads. So its not uncommon to stop the crawler and still seeing a few pages being added to the sitemap as it will wait for all responses from the target server to be processed.

After stopping the crawler you may be prompted to save all the remaining target links that had'nt been crawled yet.

<center><img src="/docs/res/queued_links_prompt.png"></center>

If you accept all the pending links will be added to the passive crawler tool.

If you deny all the pending links will be discarded.

## **Advance Crawling.**

SpiderSuite has advance crawling options:

* [Crawling target with initial seed links](#crawling-target-with-initial-seed-links)
* [Fetching list of links](#fetching-list-of-links)
* [Bruteforcing pages/directories](#bruteforcing-pagesdirectories)

This advance crawling can be accessed by clicking on the `[...]` button.

<center><img src="/docs/res/crawling_advance.png"></center> 

### **Crawling target with initial seed links**

With SpiderSuite you have the ability to provide an initial list of links (`seed links`) of the particular target and they will be added to the crawler queue of links to be crawled.

- Enter Target link
<center><img src="/docs/res/crawling_advance_crawl_target.png"></center>

- Add Seed links
<center><img src="/docs/res/crawling_advance_crawl_seed.png"></center>

_**Note:**_ The provided list of links should all relate (have the same hostname) to the main target link as the crawler uses the main target link as the reference point for all the links to be crawled.

- Click on `Crawl` to begin crawling
<center><img src="/docs/res/crawling_advance_crawl_start.png"></center>

### **Fetching list of links**
With SpiderSuite you also have the ability to fetch a provided list of links.

This type of crawling (fetching) does not crawl any additional links extrated from the crawled pages. Only the provided links will be crawled.

- You can provide file containing the list of links to be fetched. This is ideal for fectching a very long list of links as the file is not loaded into memory(it uses a streaming api to get line after line of link from the file and fetches it)

<center><img src="/docs/res/crawling_fetch_file.png"></center>

- Or you can input the list of links to be fetched. This is ideal for fetching a small to medium list of links as the list is stored in memory.

<center><img src="/docs/res/crawling_fetch_input.png"></center>

- Start the crawling by clicking on `Fetch` button.

<center><img src="/docs/res/crawling_fetch_start.png"></center>

### **Bruteforcing pages/directories**

Lastly SpiderSuite also has the ability to bruteforce target sites's directories(pages). This is a useful feature for scoping directories and files that may be hidden.

- Set the target link(url).
<center><img src="/docs/res/crawling_brute_target.png"></center>

- You can provide file containing the wordlist pages/directories to be used for bruteforcing. This is ideal for bruteforcing with a very long wordlist as the file is not loaded into memory(it uses a streaming api to get line after line of page name from the file, append it to the target link and fetch it).
<center><img src="/docs/res/crawling_brute_file.png"></center>

- Or you can input the wordlist for bruteforce. This is ideal for small to medium worldlist.
<center><img src="/docs/res/crawling_brute_input.png"></center>

- Start bruteforcing by clicking on `Bruteforce` button.
<center><img src="/docs/res/crawling_brute_start.png"></center>

## **Sitemap**

All the results from `Crawling`, `Fetching` and `Bruteforcing` will be displayed on SpiderSuite's Sitemap.

<center><img src="/docs/res/crawling_sitemap.png"></center>

The actual pages are already saved on SpiderSuite's current project database (.sspd) file.

To view content of any page on the sitemap simply click on it and all its content will be displayed on the structure and source tab.

<center><img src="/docs/res/crawling_structure.png"></center>

You can browse the structure and source tab to view all the content extracted from the particular page you clicked on.

You can perform desired actions on a page on sitemap by right clicking on it and choosing the action you want to perform.
<center><img src="/docs/res/crawling_sitemap_rightclick.png"></center>

Or You can perform desired actions on the entire list on sitemap by clicking on the `Actions` button. Please note that the Actions button is only activated if there are links on the sitemap.
<center><img src="/docs/res/crawling_sitemap_actions.png"></center>

## **Graph**

SpiderSuite has the capabilities of visualizing the links on the sitemap using a graph and also ability to manipulate the graph to your liking.

- Visualize the Entire sitemap's on a graph.

Simply click on the `Actions` button and click on `Show Graph` action to visualize the graph.
<center><img src="/docs/res/crawling_graph_actions.png"></center>

- Visualize a sitemap branch on a graph.

First change the Sitemap's view to `Tree` view.
<center><img src="/docs/res/crawling_graph_tree.png"></center>

Then Simply `right click` on the branch you want to visualize and click on `Show Graph`. This will only show the graph for that particular choosen branch.
<center><img src="/docs/res/crawling_graph_rghtclick.png"></center>

- The Graph
<center><img src="/docs/res/crawling_graph.png"></center>

- You can manipulate the graph to you linking by simply clicking on the <img src="/docs/res/config_action.png"  width=14> (`config action`) icon on graph menu bar and set your desired configurations.