# dataService-Angular
An Angular JS DataService

## Use
Inject the module into your controller, then set up the configuration for each endpoint within the controller:

```javascript
var config = {
	method: 'post',
	url: 'https://www.michaelseiler.net/api/get/my/data/',
	data: {
		// If you need to send data to the endpoint
 		someId: someId,
		someOtherId: someOtherId,
		// etc...
	}
};

// work with the response
vm.myFunction = function() {
 dataService
   .getData(config)
   .then(function(response) {
  	 // do stuff
   })
   .catch(function(err) {
     $log.warn(err);
   })
  .finally(function() {
	   // do default stuff
  });
};
```
