---
layout: page
title: Tools
menubar: docs_menu
show_sidebar: false
toc: true
hero_height: is-small
---

## **Passive Crawler Tool**
Uses OSINT (open source intelligence) sources: [waybackmachine](https://wayback.archive-it.org) and [Arquivo](https://arquivo.pt/) to obtain all publicly available url links of the target. You can use the obtained links as seed links for the next crawl.

<center><img src="/docs/res/passive_crawler_tool.png"></center>

## **SSL Certificates Tool**
Fetches SSL certificates of a particular target hostname. It does this by trying to establish a secure connection to the hostname and when done it returns the target hostname ssl certificate and closes the connection.

<center><img src="/docs/res/ssl_tool.png"></center>

## **Decoder Tool**
`Encodes`, `Decodes` or `Hashes` the input data using the choosen encoding, decoding or hashing algorithm. 
- Encoding algorithms
    - URL
    - HTML
    - Base64
    - Hex
    - Gzip
    - Brotli
- Hashing algorithms
    - Md4
    - Md5
    - Sha1
    - Sha224
    - Sha256
    - Sha384
    - Sha512
    - Sha3_224
    - Sha3_256
    - Sha3_384
    - Sha3_512
    - Keccak_224
    - Keccak_256
    - Keccak_384
    - Keccak_512

<center><img src="/docs/res/decoder_tool.png"></center>

Many other encoding,decoding and hashing algorithms will be added in the coming versions.


## **Search Tool**
Searches the current project’s data in the database and returns all the pages that contains that particular search query. The search can take a long or short period depending on the size of the project.

<center><img src="/docs/res/search_tool.png"></center>

## **Compare Tool**
Compares two different pages or crawls then highlights the differences and similarities of the two pages or crawls.

- Compare Pages
Compares two pages for any differences and similarities.
<center><img src="/docs/res/compare_pages_tool.png"></center>

- Compare Crawls
Compares two project crawls for any differences among similar pages.

<center><img src="/docs/res/compare_crawls_tool.png"></center>