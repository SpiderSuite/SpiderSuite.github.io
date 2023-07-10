# Using OTE for information gathering

You can use OSINT Template Engine to gather information about targets in two ways; using the [explorer](#explorer) window or using the [extractor](#extractor).

## Explorer

OSINT Template Engine explorer is used explore different API Endpoints offered by the available templates. When you query an endpoint, it returns the entire response on the sitemap window which you can use to analyze the result.

<center><img src="/ssuite/docs/res/explorer_in_action.gif"></center>

### Features

- You can query a single API endpoint at a time.
- You can query a single or multiple targets against a single API Endpoint at a time.
- The results are immediately stored in a database and you can view them by clicking on the sitemap corresponding item.
- You can filter templates and API endpoint depending on the input type.

### Usage

- Choose a template.
- Choose the API endpoint you want to use.
- Input respective target/targets you want to gather information on.
- Query the endpoint(start scan).
- View the results.

### Note 

- OSINT Template Engine explorer allows you to modify the templates and API endpoints for efficient custom queries.

<center><img src="/ssuite/docs/res/explorer_modify.gif"></center>

## Extractor

OSINT Template Engine extractor is used to extract and save key information from API Endpoint results offered by the available templates. It only returns the relevant key information from the result e.g. sudomains, ip and asn.

<center><img src="/ssuite/docs/res/extractor_in_action.gif"></center>

### Features

- You can query multiple API endpoints at a time.
- You can query a single or multiple targets against a single or multiple API Endpoints at a time.
- The results are immediately stored in a database and displayed on the sitemap.
- You can filter templates and API endpoint depending on the input and output type.

### Usage

- Choose the type of target input.
- Choose the type of output result you require.
- Choose the template API Endpoints you want to obtain information from.
- Input the target/targets you want to gather information on.
- Start the scan.
- The results will be accessible through the sitemap table view.

### Note 

- OSINT Template Engine extractor allows you to modify the templates, API endpoints and extractors for efficient queries.

<center><img src="/ssuite/docs/res/explorer_modify.gif"></center>
