# Redfin Scraper

![Redfin website header](https://onstock-net.fra1.cdn.digitaloceanspaces.com/apify%2Fheader.png)

## Introduction

## 📊 Actor Stats

| Stat | Value |
|------|-------|
| **Version** | `0.0.17` |
| **Last Update** | Nov 30, 2025 |

---



👋 Welcome to the Redfin Scraper. This Apify-powered actor extracts real estate data from Redfin, including detailed property listings, comparative market analysis, neighborhood information, and more. The Redfin platform offers a vast array of property details, including photos, descriptions, pricing and more. Whether you're a homebuyer, real estate investor, or market researcher, this versatile and user-friendly scraper is tailored to meet your specific needs, offering unparalleled access to Redfin's comprehensive database of residential properties across the United States.

<p align="center">
  <img src="https://apify-image-uploads-prod.s3.amazonaws.com/QcqWzAXdyfsvGKN1d/tRd64TrnPppqQFcNm-redfin.png" alt="Redfin Scraper" style="height: 60px; margin-right: 15px;" /><a href="https://apify.com/lexis-solutions/redfin-scraper" target="_blank">
    <img src="https://img.shields.io/badge/Try%20it%20on-Apify-0066FF?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDA4IiBoZWlnaHQ9IjQwOCIgdmlld0JveD0iMCAwIDQwOCA0MDgiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF8zNDFfNDE1NykiPgo8cGF0aCBkPSJNMjE4LjY5NSAxMDRIMzAwLjk3QzMwMi42NDMgMTA0IDMwNCAxMDUuMzU3IDMwNCAxMDcuMDNWMjMyLjc2NkMzMDQgMjM1Ljc3OCAzMDAuMDgzIDIzNi45NDUgMjk4LjQzNCAyMzQuNDI1TDIxNi4xNTkgMTA4LjY5QzIxNC44NDEgMTA2LjY3NCAyMTYuMjg3IDEwNCAyMTguNjk1IDEwNFoiIGZpbGw9IndoaXRlIi8+CjxwYXRoIGQ9Ik0xODkuMzA1IDEwNEgxMDcuMDNDMTA1LjM1NyAxMDQgMTA0IDEwNS4zNTcgMTA0IDEwNy4wM1YyMzIuNzY2QzEwNCAyMzUuNzc4IDEwNy45MTcgMjM2Ljk0NSAxMDkuNTY2IDIzNC40MjVMMTkxLjg0IDEwOC42OUMxOTMuMTU5IDEwNi42NzQgMTkxLjcxMyAxMDQgMTg5LjMwNSAxMDRaIiBmaWxsPSJ3aGl0ZSIvPgo8cGF0aCBkPSJNMjAyLjU5MSAyMDQuNjY4TDEwOS4xMjcgMjk4LjgzNUMxMDcuMjI5IDMwMC43NDcgMTA4LjU4MyAzMDQgMTExLjI3OCAzMDRIMjk2LjhDMjk5LjQ4MyAzMDQgMzAwLjg0MiAzMDAuNzcgMjk4Ljk2NyAyOTguODUyTDIwNi45MDggMjA0LjY4NUMyMDUuNzI2IDIwMy40NzUgMjAzLjc4MiAyMDMuNDY4IDIwMi41OTEgMjA0LjY2OFoiIGZpbGw9IndoaXRlIi8+CjwvZz4KPGRlZnM+CjxjbGlwUGF0aCBpZD0iY2xpcDBfMzQxXzQxNTciPgo8cmVjdCB3aWR0aD0iMjAwIiBoZWlnaHQ9IjIwMCIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEwNCAxMDQpIi8+CjwvY2xpcFBhdGg+CjwvZGVmcz4KPC9zdmc+Cg==&logoColor=white" alt="Try it on Apify" style="border-radius: 12px; height: 60px;" />
  </a>
</p>


## Use Cases

Redfin Scraper can be employed across a variety of use cases:

1. **Real estate research:** Gather data on specific locations, property types, and price ranges to inform real estate research and decision-making processes.
2. **Investment analysis:** Identify undervalued properties or areas where investment opportunities may be present, by comparing various properties, locations, and market trends.
3. **Market trend tracking:** Keep an eye on real estate trends in neighborhoods or cities of interest to stay ahead of the curve and capitalize on market opportunities.
4. **Mortgage or rent payment analytics:** Use scraped data to better understand the optimal mortgage or rental payment amounts for various properties based on factors, such as property value, area, and overall market conditions.
5. **Appraisal management:** Automate the process of appraising properties for clients by rapidly comparing property values, historical sales, and market averages across a range of conditions.
6. **Lead generation:** Identify and qualify suitable leads for real estate professionals based on preferences, potential interest, and budget.

Happy scraping!

## Input 📥

To use this actor, you need to provide the following input:

- Field: **startUrls**
  - Type: array
  - Required: Yes
  - Description: Search or property URLs to scrape
- Field: **mode**
  - Type: string
  - Required: Yes
  - Description: The mode scraping. (rent or buy)
- Field: **maxPages**
  - Type: integer
  - Required: No
  - Description: The number of pages to be scraped. (if search)
- Field: **proxyConfiguration**
  - Type: object
  - Required: No
  - Description: Your proxy configuration from Apify

## How to get start urls?

1. A single listing

   Open the propertly listing on [Redfin](https://www.redfin.com) and copy its link from the browser URL bar.

2. Search

   2.1. Open the [Redfin](https://www.redfin.com) website.

   2.2. Enter the location you are interested in and hit the search button.

   2.3. Once in the search page, add all needed filters on the page. This will change the URL in the browser search bar. Once ready, copy the URL and paste to Apify as an item in the `startUrl` array.

### Examples

A single listing:

```
https://www.redfin.com/AK/Anchorage/1353-W-27th-Ave-99503/apartment/131078309
```

A search page (rents in Anchorage under $1150/mo)

```
https://www.redfin.com/city/781/AK/Anchorage/apartments-for-rent/filter/max-price=1.15k
```

## Output 📤

An example output for buy mode looks like this:

```json
{
  "status": "Active",
  "id": 14772,
  "price": 374000,
  "community": "Westlake",
  "mls": "2048796",
  "yearBuild": 1977,
  "propertyType": "Condo",
  "bathsFull": 1,
  "beds": 1,
  "pricePerSqFt": 569,
  "agentCommission": "3%",
  "description": "Queen Anne beauty with open floor plan &amp; updates throughout! Gorgeous views of Lake Union welcome you to this bright, stylish top floor unit. Fully updated kitchen with SS appliances &amp; subway tile backsplash flows to the open living room with a wall of windows so you can always take in the amazing views! Beautiful balcony to enjoy on those warmer spring/summer days as well. Large primary bedroom &amp; bathroom with updated vanity and a great skylight so it&rsquo;s always bright. New w/d in 2021, new water heater in 2018. Half a block from Lake Union: immediate bike path access and easy pedestrian access to SLU, Fremont, and DT Seattle. Easy car commuting &amp; near routes on Dexter. Storage locker, secure parking, &amp; no rental cap. Hurry to your new home! ",
  "soldDate": "2005-11-02T08:00:00.000Z",
  "sqFt": 657,
  "streetAddress": "762 Hayes St #44",
  "timeOnRedfin": "0 days",
  "agent": {
    "agentName": "Osama Khalaf",
    "agentUrl": "https://www.redfin.com/real-estate-agents/osama-khalaf",
    "brokerName": "Redfin"
  },
  "mapUrl": "https://maps.google.com/maps/api/staticmap?sensor=false&style=feature%3Aadministrative.land_parcel%7Cvisibility%3Aoff&style=feature%3Alandscape.man_made%7Cvisibility%3Aoff&style=feature%3Atransit.station%7Chue%3A0xffa200&center=47.6341205%2C-122.3414566&channel=desktop_xdp_above_fold_static_preview&size=200x200&scale=1&format=jpg&zoom=10&client=gme-redfin&signature=o_-HMR79x285XXRXsDJ2qVsExLs=",
  "address": {
    "countryCode": "US",
    "city": "Seattle",
    "streetAddress": "762 Hayes St #44",
    "zip": "98109"
  },
  "photos": [
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_32.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_26.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_27.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_28.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_29.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_30.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_33.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_3.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_4.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_5.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_6.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_22.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_23.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_24.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_20.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_8.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_11.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_12.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_13.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_14.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_15.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_16.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_17.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_19.webp",
    "https://ssl.cdn-redfin.com/system_files/media/803489_JPG/genLdpUgcFull/item_31.webp"
  ]
}
```

An example output for rent mode looks like this:

```json
{
  "id": 131034334,
  "price": 950,
  "streetAddress": "3401 Eureka St"
}
```

## Need to scrape other real estate websites?

👉 Scrape Switzerland Properties with [FlatFox.ch Scraper](https://apify.com/lexis-solutions/flatfox-ch-properties-scraper)

👉 Scrape Denmark Properties with [Boligsiden.dk Scraper](https://apify.com/lexis-solutions/boligsiden-dk-scraper)

## FAQ 💬

**Q: How do I provide the searchUrl?**

A: To provide the searchUrl, first perform a search on Redfin.com using their search bar. Browse the results page, and then copy and paste the URL from your web browser to the appropriate field in the scraper's input configuration.

**Q: Can I filter the search results before running the scraper?**

A: Yes, you can use filters available on Redfin.com, such as price range, number of bedrooms, home types, etc., to narrow down your search. The scraper will extract the data based on your specified filters.

**Q: I'm getting CAPTCHAs (403 errors in the run logs). How can I avoid getting blocked by the website?**

A: For best results we recommend using a **residential proxy** from Apify. You can select this when starting the actor.

**Q: I'm seeing "The version has been changed" in the run logs. Should I worry?**

A: The actor tracks the version of the website, and shows a warning when the site changes. In most cases, this should not be a problem for the data extraction. However, if you see any discrepancies, make sure to send a bug report via the Apify console.
