# Hp Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Hp Scraper](https://oxylabs.io/products/scraper-api/ecommerce/hp?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Hp website effortlessly. This brief guide showcases how Hp Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Hp results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Hp page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.hp.com/us-en/shop/cat/laptops'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/hp-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html>\n    <html lang=\"en-us\">\n      <head>\n        <script>window.dataLayer = window.dataL ... </html>",
      "created_at": "2024-02-20 12:50:06",
      "updated_at": "2024-02-20 12:50:07",
      "page": 1,
      "url": "https://www.hp.com/us-en/shop/cat/laptops",
      "job_id": "7165689071765856257",
      "status_code": 200
    }
  ]
}
```
With our Hp Scraper, you can seamlessly harvest public data from any Hp laptop or printer web page. Gather important product data such as the cost, customer feedback, or detailed descriptions to deepen your market insights and outperform your rivals. Should you require assistance, don't hesitate to engage our support team on live chat or email us at hello@oxylabs.io.