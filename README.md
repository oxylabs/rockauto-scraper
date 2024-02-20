# Rockauto Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Rockauto Scraper](https://oxylabs.io/products/scraper-api/ecommerce/rockauto?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Rockauto website effortlessly. This brief guide showcases how Rockauto Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Rockauto results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Rockauto page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.rockauto.com/en/catalog/ford'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/rockauto-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE HTML>\n<html class=\"no-js \" lang=\"en\">\n<head>\n<meta http-equiv=\"content-type\" content=\"text ... </html>",
      "created_at": "2024-02-20 12:57:28",
      "updated_at": "2024-02-20 12:57:29",
      "page": 1,
      "url": "https://www.rockauto.com/en/catalog/ford",
      "job_id": "7165690923681083393",
      "status_code": 200
    }
  ]
}
```
Using our Rockauto Scraper, you can easily amass public data from any Rockauto web page. Accumulate necessary information on car parts, such as pricing, customer reviews, or detailed descriptions, to keep track of the automotive industry and outperform your competitors. If you need assistance or have any queries, feel free to reach our support team through live chat or simply email us at hello@oxylabs.io.