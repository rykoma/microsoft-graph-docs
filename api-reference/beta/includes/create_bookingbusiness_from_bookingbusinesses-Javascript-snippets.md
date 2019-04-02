
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const bookingBusinesses = {
    displayName:"Fourth Coffee",
    address:{
        type:"mall",
        postOfficeBox:"P.O. Box 123",
        street:"4567 Main Street",
        city:"Buffalo",
        state:"NY",
        countryOrRegion:"USA",
        postalCode:"98052"
    },
    phone:"206-555-0100",
    email:"manager@fourthcoffee.com",
    webSiteUrl:"https://www.fourthcoffee.com",
    defaultCurrencyIso:"USD"
}
;

//make the request to Graph
try{
	let res = await client.api('/bookingBusinesses')
		.version('beta')
		.post({bookingBusiness : bookingBusinesses});
	console.log(res);
} catch (error) {
	throw error;
}

```