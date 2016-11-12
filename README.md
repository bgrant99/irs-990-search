IRS Form 990-PF Search
======================

This is a sample project which uses [Algolia](http://www.algolia.com) to implement instant-search of the IRS Form 990 index files hosted on [Amazon AWS](https://aws.amazon.com/public-datasets/irs-990/).

It's goal is to demonstrate the use of hosted microservices to create near maintenance-free alternatives to complex, home-built search capabilities.

*Note: We've limited the data to be searched to Form 990-PF only*

## Usage

*This is a fork of Algolia's [Instant Search Demo](https://github.com/algolia/instant-search-demo). Please view the README on that project for detailed instructions including links to a step by step tutorial.*

1) Create your free Algolia account and upload the `index.json` file located in `_data`, naming the index `filings_pf_grouped_by_ein` 

2) In the Algolia dashboard, adjust the settings as follows:  

- `Indices > Rankings > Basic Settings`  
  - Add a Searchable Attribute (click `OrganizationName`)  
  - Add a Custom Ranking Attribute (click `Filings.TaxPeriod`)  

3) Replace the demo credentials with your own:
- in `assets/js/app.js`, set your own `APPLICATION_ID`  
- in `assets/js/app.js`, set your own `SEARCH_ONLY_API_KEY`  
- in `assets/js/app.js`, set your own `INDEX_NAME`  

4) Update `_config.yml`, removing our demo url from the `url` field.  

5) Your app will be live at:  
https://YOURUSERNAME.github.io/irs-990-search/  

## License

SmarterGiving logo (c) Chad Kruse, SmarterGiving - All Rights Reserved

The MIT License (MIT)

Copyright (c) 2015 Algolia - Original Work  
Copyright (c) 2016 Chad Kruse, SmarterGiving - Modifications

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
