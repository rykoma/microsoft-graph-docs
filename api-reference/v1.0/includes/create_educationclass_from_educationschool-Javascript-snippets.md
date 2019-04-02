
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const classes = {
 @odata.id:"https://graph.microsoft.com/v1.0/education/classes/11006"
};

//make the request to Graph
try{
	let res = await client.api('/education/schools/{school-id}/classes/$ref')
		.post({educationClass : classes});
	console.log(res);
} catch (error) {
	throw error;
}

```