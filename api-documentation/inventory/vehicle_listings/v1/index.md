---
layout: api-documentation
title : 'Vehicle Inventory Listings'
title_active_left_menu: 'Vehicle Listings'
title_parent: Api documentation

amount_version: 1
spec: vehicle_listings
version: v1
api: inventory
dropdown-link: 'Select an Endpoint'


level: 2
overview: page_version
---

#### This resource provides a list of cars available for sale at a specific dealership.

### Sort options

You can sort by the following properties with either **|asc** or **|desc** appended to it. For example, if you want to search by ascending price, you set sort to **price|asc** (i.e. sort=price|asc).

If you want to sort by **multiple properties**, you should separate them by comma. Example, *sort|price:asc,distance|asc*

You can sort on any *request parameter* list for a particular endpoint.


### Filter options

You can use the basicFilter query string parameter to filter out the results. You can add as many *basicFilter=value* key/value pairs to the query string. The value of the basicFilter has to follow this format:

***basicFilter=key:"valye"***

*The double quotes are important.*

You can use the basicFilter wit any *response key* for a particular endpoint.