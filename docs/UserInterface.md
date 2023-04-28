---
layout: page
title: User Interface
menubar: docs_menu
show_sidebar: false
toc: true
hero_height: is-small
---

# **Main Window**
SpiderSuite’s Main window contains the following information.

<center><img src="/docs/res/mainwindow.png"/></center>

- [Menu & Tool bar](#menu--tool-bar)
- [Sitemap View](#sitemap-view)
- [Request View](#request-view)
- [Structure View](#structure-view)
- [Source View](#source-view)
- [Graph View](#graph-view)

## **Menu & Tool Bar**

Contains actions that can be performed on the application and the project.

- **Application**

    - **Open** - opens a project from the file system.

    - **Open Recent** - shows and opens recent SpiderSuite projects you’ve been working on.

    - **Import From** - Imports links and their data from other tools and file types such as:
        - Links from CSV files
        - Links from Sitemap files
        - Links from Zed Attack Proxy(ZAP),
        - Links from acunetix(.xml files),
        - Data from Fiddler(.saz files),
        - Data exported from BurpSuite(.xml files),
        - Data from HTTP Archives(.har files)
        - Data from Caido (CSV & JSON files)
        - Data from Katana crawler (INDEX and JSON files)

    - **Save** - Saves the current project you’re working on without closing it.

    - **Clear** – Clears and deletes all the data of the current loaded project.

    - **Close** - closes the current loaded project without deleting any data from that particular project.

    - **Exit** - Closes the application.

- **Tools**

    - **Search Tool** – Searches the current project’s data in the database and returns all the pages that contains that particular search query. The search can take a long or short period depending on the size of the project.

    - **Decoder Tool** – Encodes, Decodes or hashes the input data using the choosen encoding, decoding or hashing algorithm. Many other encoding,decoding and hashing algorithms will be added in the coming versions.

    - **Compare Tool** - compares two different pages or crawls then highlights the differences and similarities of the two pages or crawls. 

    - **SSL certificates Tool** - Fetches SSL certificates of a particular target hostname. It does this by trying to establish a secure connection to the hostname and when done it returns the target hostname ssl certificate and closes the connection.

    - **Passive Crawler Tool** - Uses OSINT (open source intelligence) sources such as [waybackmachine](https://archive.org) to obtain all publicly available url links of a particular target. You can use the obtained links as seed links for the next crawl as it broadens the crawlers scope.

- **Options**

    - **Preferences** - All program’s settings and scan configurations.

- **Help**

    - **Log Viewer** – Displays all scan and program logs.

    - **Donate** - Takes you to a page for donating to the SpiderSuite project.

    - **Blog** - Takes you to SpiderSuite blog where all you can find all articles and documentation on SpiderSuite.

    - **Twitter** - Takes you to SpiderSuite’s twitter page.

    - **Github** - Takes you to SpiderSuite’s Github repository page.

    - **Check For Updates** - checks for any available updates on SpiderSuite.

    - **About** - Information about SpiderSuite.

    - **About Qt** - Information about Qt C++ Framework used to create SpiderSuite.

## **Sitemap View**

Displays the crawled pages or pages imported from other tools.

- **Types ComboBox** - Filters the types of pages to display on the sitemap i.e:
    - All (displays all page type)
    - HTML (displays only html files)
    - Javascript (displays only javascript files)
    - CSS (displays only CSS files)
    - JSON (displays only JSON files)
    - XML (displays only XML files)
    - Image (displays only image files)
    - Audio (displays only audio files)
    - Video (displays only video files)
    - Documents (displays only document files)
    - Database (displays only database files)
    - Archive (displays only archive files)
    - Binary (displays only binary files)
    - Font (displays only font files)
    - Misc (displays miscelleneous files)

- **List** - Displays the pages crawled in a list format

- **Tree** - Displays the pages crawled in a tree hierrachical structure

- **[Action >] button** - Provides a menu of actions that you can perform on the displayed sitemap pages.

## **Request View**

Perfoms HTTP(S) request on the provided target then saves and display the results.

This feature is useful for performing manual tests on a target. The request are sent one after another and you can only send another request when the previous request has elicited a response.

- **HTTP version ComboBox** - Choose the HTTP verison (HTTP/1.X or HTTP/2.X) to use for request.

- **Method type ComboBox** - Choose the Method(GET,POST,PUT,DELETE) to use for HTTP request.

- **Headers List** - Input request headers to use for request.

- **Query data TextEdit** - Input the query data to send with request for POST & PUT methods only.

- **History List** - Displays the pages that you have requested, you can access the pages content by simply clicking on them.

## **Structure View**

Displays the contents extracted from the crawled pages. Click on a page in Sitemap or Request History to access the page's contents in structure view.

- **Page Tab** - Displays basic information extracted from the page such as size,content type,method used and all links extracted from the page.

- **Headers Tab** - Displays all the request and response headers extracted from the http request and response.

- **Cookies Tab** - Displays all the request and response cookies extracted from the http request and response headers.

- **Meta Tab** - Displays all the meta information extracted from the `<meta>` tag in html page.

- **Comments Tab** - Displays all the code comments extracted from the page source.

- **Scripts Tab** - Displays all the javascript code extracted from the `<script>` html tag.

- **Styles Tab** - Displays all the CSS code extracted from the `<style>` html tag.

- **Forms Tab** - Displays all the html forms extacted from the html `<form>` tag.

- **Wappalyzer Tab** - Detects and Displays all the web technologies used on that page.

## **Source View**

Displays the source (response body) of the crawled page. Click on a page in Sitemap or Request History to access the page's source in Source view.

- **Text View** - Displays the page's source in Text format.
- **Hex View** - Displays the pages's source in Hexadecimal format.
- **Tree view** - Displays the page's source in a tree format (available for html, xml, json and css files only for now).
- **Image View** - Displays the image (available for image files only)

## **Graph View**

Visualizes the crawled pages on a graph. Visualizes either the entire sitemap of a branch of the pages from the sitemap tree view.

Uses two types graph layouts (Dot and SFDP layout), three types of node shapes (Rectangle, ellipticle and point shapes) and node colors of your choosing.