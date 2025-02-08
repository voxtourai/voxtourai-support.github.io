---
layout: default
title: API References
parent: API
description: VoxTour.ai provides a powerful API for integrating AI-powered audio guides and travel experiences into applications, websites, and services. Our API enables seamless access to high-quality, location-based storytelling, allowing users to explore destinations with engaging narratives, historical insights, and personalized recommendations.
---

# API References

VoxTour.ai provides a powerful API for integrating AI-powered audio guides and travel experiences into applications, websites, and services. Our API enables seamless access to high-quality, location-based storytelling, allowing users to explore destinations with engaging narratives, historical insights, and personalized recommendations.
<details>
<summary>Search POIs by different criteria</summary>
<div class="api-url-box">POST https://api.voxtour.ai/v1/queryPOIs</div>
<div>The POI Query API allows users to search for Points of Interest (POIs) within a specified geographical area based on keywords, categories, or ranking criteria. The API returns a structured list of POIs with details such as name, description, location, images, and metadata.</div>
<h3>Key Features</h3>
<ol>
<li>Search POIs by different criteria (e.g., keyword, location, language)</li>
<li>Filter results using a bounding box (latitude/longitude)</li>
<li>Sort results by relevance or custom criteria</li>
<li>Retrieve detailed POI information, including descriptions, images, and external links</li>
</ol>
<h3>Example Request</h3>
<div>Querying for POIs named "Tower" within a defined bounding box:</div>
{% highlight json %}
{
   "apiKey": "12345678-90ab-cdef-1234-567890abcdef",
   "lang": "en",
   "search": "Tower",
   "boundingBox": [
       43.300000,
       44.100000,
       -80.000000,
       -78.500000
   ],
   "firstSortBy": null,
   "firstSortDescending": false,
   "secondSortBy": null,
   "secondSortDescending": false,
   "pageSize": 200,
   "pageNumber": 1
}
{% endhighlight %}
<h3>Example Response</h3>
Returns a list of matching POIs, including name, description, coordinates, and images:
{% highlight json %}
{
   "poiList": [
       {
           "poiId": "87a1478a-7363-4dc4-818a-141eff446880",
           "name": "CN Tower",
           "info": "The CN Tower, officially known as 'Tour CN,' is a prominent communications and observation tower located in downtown Toronto, Ontario, Canada. Completed in 1976, it stands at 553.3 meters (1,815 feet) and was the world's tallest free-standing structure for over three decades.",
           "nativeName": "CN Tower",
           "category": "ArchitecturalMarvel",
           "subcategory": "Skyscraper",
           "address": "CN Tower, 290, Bremner Boulevard, Harbourfront, Spadina—Fort York, Old Toronto, Toronto, Ontario, M5V 3L9, Canada",
           "latitude": 43.6425637,
           "longitude": -79.38708718320467,
           "imageList": [
               {
                   "imageUrl": "https://upload.wikimedia.org/wikipedia/commons/thumb/e/e6/CN_Tower_1.jpg",
                   "sourceUrl": "https://commons.wikimedia.org/wiki/File:CN_Tower_1.jpg",
                   "attributionHtml": "<a href=\"https://commons.wikimedia.org/wiki/File:CN_Tower_1.jpg\">Giorgio Galeotti</a>, <a href=\"https://creativecommons.org/licenses/by/4.0\">CC BY 4.0</a>, via Wikimedia Commons"
               },
               {
                   "imageUrl": "https://upload.wikimedia.org/wikipedia/commons/thumb/9/90/CN_Tower_2.jpg",
                   "sourceUrl": "https://commons.wikimedia.org/wiki/File:CN_Tower_2.jpg",
                   "attributionHtml": "<a href=\"https://commons.wikimedia.org/wiki/File:CN_Tower_2.jpg\">Ken Lund from Reno, Nevada, USA</a>, <a href=\"https://creativecommons.org/licenses/by-sa/2.0\">CC BY-SA 2.0</a>, via Wikimedia Commons"
               }
           ],
           "hashtagMap": {},
           "metadata": [
               {
                   "name": "wikipedia",
                   "value": "en:CN Tower",
                   "timestamp": "2024-06-03T12:17:00.568101Z"
               },
               {
                   "name": "website",
                   "value": "https://www.cntower.ca/",
                   "timestamp": "2024-05-26T02:48:45.475446Z"
               }
           ],
           "rank": 0.8958864102649058
       }
   ]
}
{% endhighlight %}
</details>
<details>
<summary>Create Tour Route.</summary>

The POI Query API allows users to search for Points of Interest (POIs) within a specified geographical area based on keywords, categories, or ranking criteria. The API returns a structured list of POIs with details such as name, description, location, images, and metadata.

*Key Features*
1. Search POIs by different criteria (e.g., keyword, location, language).
2. Filter results using a bounding box (latitude/longitude).
3. Sort results by relevance or custom criteria.
4. Retrieve detailed POI information, including descriptions, images, and external links

*Example Request*
</details>