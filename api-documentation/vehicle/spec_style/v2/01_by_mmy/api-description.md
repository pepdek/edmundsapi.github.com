---
layout: api-documentation
title : 'Get Car Style Details by Car Make/Model/Year'
title_active_left_menu: "Spec: Style"
title_parent: Api documentation

amount_version: 2
title-endpoint: 'Get Car Style Details by Car Make/Model/Year'
spec: spec_style
version: v2
api: vehicle
dropdown-link: 'api/vehicle/v2/{make}/{model}/{year}/styles'


level: 3
description_edpoint: 'Get Car Style Details by Car Make/Model/Year'
title_md : Description
number: 1

---

### Description

Get the vehicle style details (i.e. colors, options, transmission, engine, squishVins, ...etc) by the vehicle's Make/Mode/Year information. The style ID of a vehicle is **available** in the responses of the *model* and *model year* endpoints.

### URL

	https://api.edmunds.com/api/vehicle/v2/{make}/{model}/{year}/styles?fmt=json&api_key={api key}
	
### Code Example

You need the [Javascript SDK](https://github.com/EdmundsAPI/edmunds-javascript-sdk) to run this example.

	<!DOCTYPE html>

	<html>
	<head>
		<meta charset=utf-8>
		<title>Edmunds API Example</title>
	</head>

	<body>
		<div id="results-body"></div>
		<script>
		  	window.sdkAsyncInit = function() {
		    	// Instantiate the SDK
				var res = new EDMUNDSAPI('YOUR API KEY');

				// Optional parameters
				var options = {};

				// Callback function to be called when the API response is returned
				function success(res) {
					var body = document.getElementById('results-body');
					body.innerHTML = "The first style name is: " + res.styles[0].name;
				}

				// Oops, Houston we have a problem!
				function fail(data) {
					console.log(data);
				}

				// Fire the API call
				res.api('/api/vehicle/v2/lexus/rx350/2011/styles', options, success, fail);

			    // Additional initialization code such as adding Event Listeners goes here
		  };

		  // Load the SDK asynchronously
		  (function(d, s, id){
		     	var js, sdkjs = d.getElementsByTagName(s)[0];
		     	if (d.getElementById(id)) {return;}
		     	js = d.createElement(s); js.id = id;
		     	js.src = "path/to/sdk/file";
		     	sdkjs.parentNode.insertBefore(js, sdkjs);
		   }(document, 'script', 'edmunds-jssdk'));
		</script>
	</body>
	</html>