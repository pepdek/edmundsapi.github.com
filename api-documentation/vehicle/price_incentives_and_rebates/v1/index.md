---
layout: api-documentation
title : 'Price: Incentives and Rebates'
title_active_left_menu: 'Price: Incentives and Rebates'
title_parent: Api documentation

amount_version: 1
spec: price_incentives_and_rebates
version: v1
api: vehicle
dropdown-link: 'Select an Endpoint'


level: 2
overview: page_version

---

<div class="info-message">
	This resource is about getting incentives and rebates for vehicles. To fully understand the data you get back from the endpoints available in this resource, you will need to understand a few key concepts, like what incentives types, <em>source</em> types and <em>content</em> types there are.
</div>

### Endpoints

* [Get Incentives & Rebates Information by ID](/api-documentation/vehicle/price_incentives_and_rebates/v1/01_findbyid/api-description.html)
* [Get Incentives & Rebates for a Specific Car Category](/api-documentation/vehicle/price_incentives_and_rebates/v1/02_findincentivesbycategoryandzip/api-description.html)
* [Get Incentives & Rebates Information for a Car Make ID](/api-documentation/vehicle/price_incentives_and_rebates/v1/03_findincentivesbymakeid/api-description.html)
* [Get Incentives & Rebates Information for a Car Make ID and ZIP Code](/api-documentation/vehicle/price_incentives_and_rebates/v1/04_findincentivesbymakeidandzip/api-description.html)
* [Get Incentives & Rebates Information for a Car Model Year ID and ZIP Code](/api-documentation/vehicle/price_incentives_and_rebates/v1/05_findincentivesbymodelyearidandzip/api-description.html)
* [Get Incentives & Rebates Information for a Car Style ID](/api-documentation/vehicle/price_incentives_and_rebates/v1/06_findincentivesbystyleid/api-description.html)
* [Get Incentives & Rebates Information for a Car Style ID and ZIP Code](/api-documentation/vehicle/price_incentives_and_rebates/v1/07_findincentivesbystyleidandzipcode/api-description.html)

### Incentives Types

* CASH_REBATE
* LOW_APR
* LEASE
* MISCELLANEOUS

### Incentives Source Types (i.e. *sourceType*)

* AAA
* AARP
* Aged Inventory
* American Quarter Horse Association
* APR
* Auto Show
* Associated Builders and Contractors (ABC)
* Bonus Cash
* Conquest
* Customer Cash
* Customer Cash or APR
* IUPA and NAPO
* Lease Bonus Cash
* Lender
* Loyalty
* Military
* Mobility
* National Thoroughbred Racing Association
* NCAF (National Community Action Foundation)
* NRA
* Percentage
* Plumbing, Heating and Cooling Association
* Preferred Price
* Service Roundtable Association
* Student/College Grad
* Texas and Southwestern Cattle Raisers Association
* Texas Coastal Conservation Association
* Trade Assistance

### Incentives Content Type (i.e. *content_type*)
                                                                                          
| content_type      		| Description                         																		|
|:--------------------------|:----------------------------------------------------------------------------------------------------------|
| Customer APR		    	| A loan, offered by the manufacturer's captive finance company, at a below-market interest rate. Normally eligibility is limited based on the customer's credit worthiness.|
| Customer Bonus Cash		| Customer cash, with specific requisites, that may or may not be combined with other incentives. Examples include college grad cash and military cash.|
| Customer Cash 			| A rebate offered by the manufacturer to the customer to adjust downward the net price of the vehicle.|
| Customer Cash or APR  	| A choice of the customer between Manufacturer to customer cash incentive and a customer low APR loan.|
| Customer Cash and APR		| A combination of a customer rebate and a low APR loan. Customer Cash or APR A choice of the customer between a rebate and a low APR loan.	|
| Lease						| A special lease that is offered by the manufacturer to stimulate sales by lowering the customer's monthly payment through subsidizing the vehicle's Residual Value or Money Factor.|
| Text Only					| Incentives that don’t involve a specific customer cash, or APR figure. For example, an incentive to receive a free Ipod would be text only. |

The <code>primary</code> property in the response will always be **false** when the contentType is ***Customer APR*** or ***Lease*** or ***Customer Cash And APR***
 
The <code>primary</code> property *CAN* be set to **true** when contentType is ***Customer Cash*** or ***Customer Bonus Cash*** or ***Customer Cash or APR*** (but **primary** doesn’t always equal true just because the contentType is mentioned above.)
 
When *contentType* is ***Customer Bonus Cash*** AND *primary* is **false**, then it is best to check <code>sourceType</code> property to see if the bonus cash is available to specific group (i.e. Military, College, Lender, ...etc).

                                                                                         





