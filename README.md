# ![LOGO](logo.png) Owler **flow**ground Connector

## Description

A generated **flow**ground connector for the Owler API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/owler.com/1.0.0/swagger.json<br/>
Generated at: 2019-06-06T16:13:04+03:00

## API Description

Search for information on companies using a website or company name and get access to Company Data, News, Blog Posts, Competitor Lists and much more.

## Authorization

Supported authorization schemes:
- API Key
## Actions

### Basic Search Company by Ticker or Website or Name or PermID

> The Company Basic Search API searches for a company based on the input and will returns results containing basic details about matching companies. By default the API returns the top 10 available results unless the limit is specified. The maximum limit is restricted to 30.

*Tags:* `CompanyAPI`

#### Input Parameters
* `q` - _required_ - Search term
* `fields` - _optional_ - Fields to be searched - name, website, ticker, permid. If not specfied, will be searched against all fields
* `limit` - _optional_ - Number of results to be displayed - 10 (by default, if not specified) to 30
* `format` - _optional_ - Format of the response content - json (by default if not specified), xml
    Possible values: xml, json.

### Get Competitor information by Id

> The Competitors API provides basic information about top 3 competitors of a company specified in the Company Id

*Tags:* `CompetitorAPI`

#### Input Parameters
* `companyId` - _required_ - Company Id
* `format` - _optional_ - Format of the response content - json (by default if not specified), xml
    Possible values: xml, json.

### Get Competitor information by URL

> The Competitors API provides basic information about top 3 competitors of a company specified in the website

*Tags:* `CompetitorAPI`

#### Input Parameters
* `website` - _required_ - Company Id
* `format` - _optional_ - Format of the response content - json (by default if not specified), xml
    Possible values: xml, json.

### Get Competitor information by Id

> The Competitors API provides basic information about all competitors of a given company Id

*Tags:* `CompetitorPremiumAPI`

#### Input Parameters
* `companyId` - _required_ - Company Id
* `pagination_id` - _optional_ - Pass pagination_id as * in the first API request. The API response will return top competitors along with the next pagination_id which can be passed in the subsequent API request to get the next set of competitors. Repeat this process until needed or till the pagination_id returned is blank. Note:Every response will have maximum of 50 competitors.
* `format` - _optional_ - Format of the response content - json (by default if not specified), xml
    Possible values: xml, json.

### Get Competitor information by Url

> The Competitors API provides basic information about all competitors of a given company Id

*Tags:* `CompetitorPremiumAPI`

#### Input Parameters
* `website` - _required_ - Company Id
* `pagination_id` - _optional_ - Pass pagination_id as * in the first API request. The API response will return top competitors along with the next pagination_id which can be passed in the subsequent API request to get the next set of competitors. Repeat this process until needed or till the pagination_id returned is blank. Note:Every response will have maximum of 50 competitors.
* `format` - _optional_ - Format of the response content - json (by default if not specified), xml
    Possible values: xml, json.

### Fuzzy Search Company by Name or Address or Phone

> The Company Fuzzy Search API searches for a company based on the input and will return results containing basic details about matching companies. By default the API returns at most top 10 available results unless the limit is specified. The maximum limit is restricted to 30.

*Tags:* `CompanyAPI`

#### Input Parameters
* `q` - _required_ - Search term
* `fields` - _required_ - Fields to be searched - name, website, ticker, permid, address, phone. Each field and its corresponding value has to be specified
* `limit` - _optional_ - Number of results to be displayed - 10 (by default, if not specified) to 30
* `format` - _optional_ - Format of the response content - json (by default if not specified), xml
    Possible values: xml, json.

### Get Company by Id

> The Company Data API provides complete information about a company for the specified Company Id

*Tags:* `CompanyAPI`

#### Input Parameters
* `companyId` - _required_ - Company Id
* `format` - _optional_ - Format of the response content - json (by default if not specified), xml
    Possible values: xml, json.

### Search Company by Ticker or Website or Name or PermID

> The Company Search API searches for a company based on the input and will returns results containing basic details about matching companies. By default the API returns the top 10 available results unless the limit is specified. The maximum limit is restricted to 30.

*Tags:* `CompanyAPI`

#### Input Parameters
* `q` - _required_ - Search term
* `fields` - _optional_ - Fields to be searched - name, website, ticker. If not specified, will be searched against all fields
* `limit` - _optional_ - Number of results to be displayed - 10 (by default, if not specified) to 30
* `format` - _optional_ - Format of the response content - json (by default if not specified), xml
    Possible values: xml, json.

### Get Company by URL

> The Company Data API provides complete information about a company for the specified URL

*Tags:* `CompanyAPI`

#### Input Parameters
* `website` - _required_ - Company Domain
* `format` - _optional_ - Format of the response content - json (by default if not specified), xml
    Possible values: xml, json.

### Get Complete Company Info by Id

> The Company Premium Data API provides complete information about a company for the specified Company Id

*Tags:* `CompanyPremiumAPI`

#### Input Parameters
* `companyId` - _required_ - Company Id
* `format` - _optional_ - Format of the response content - json (by default if not specified), xml
    Possible values: xml, json.

### Get Basic Company Info by Url

> The Company Data API provides complete information about a company for the specified URL

*Tags:* `CompanyPremiumAPI`

#### Input Parameters
* `website` - _required_ - Company Domain
* `format` - _optional_ - Format of the response content - json (by default if not specified), xml
    Possible values: xml, json.

### Get Feeds for given Company Ids

> The Feeds API provides a list of feeds and individual feed information for the given Company Ids and Category. By default the API returns the latest 10 feeds available unless the limit is specified. The maximum result is restricted to 100 feeds per API request.

*Tags:* `FeedAPI`

#### Input Parameters
* `format` - _optional_ - Format of the response content - json (by default if not specified), xml
    Possible values: xml, json.
* `company_id` - _required_ - Company Ids separated by comma (Maximum of 150 Company Ids)
* `limit` - _optional_ - Number of results to be displayed - 10 (by default, if not specified) to 100
* `pagination_id` - _optional_ - Pass pagination_id as blank in the first API request. The API response will return the latest feeds along with the next pagination_id which can be passed in the subsequent API request to get the next set of feeds. Repeat this process until needed or till the pagination_id returned is blank
* `category` - _optional_ - Categories separated by comma. If not specified, will search against all categories

### Get Feeds for given Company Websites

> The Feeds API provides a list of feeds and individual feed information for the given Company Websites and Category. By default the API returns the latest 10 feeds available unless the limit is specified. The maximum result is restricted to 100 feeds per API request.

*Tags:* `FeedAPI`

#### Input Parameters
* `format` - _optional_ - Format of the response content - json (by default if not specified), xml
    Possible values: xml, json.
* `domain` - _required_ - Company Websites separated by comma (Maximum of 10 Company Websites)
* `limit` - _optional_ - Number of results to be displayed - 10 (by default, if not specified) to 100
* `pagination_id` - _optional_ - Pass pagination_id as blank in the first API request. The API response will return the latest feeds along with the next pagination_id which can be passed in the subsequent API request to get the next set of feeds. Repeat this process until needed or till the pagination_id returned is blank
* `category` - _optional_ - Categories separated by comma. If not specified, will search against all categories

## License

**flow**ground :- Telekom iPaaS / owler-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
