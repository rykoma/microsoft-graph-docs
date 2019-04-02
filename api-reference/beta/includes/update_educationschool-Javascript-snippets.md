
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const schools = {
  displayName: "Fabrikam Arts High School",
  description: "Magnate school for the arts. Los Angeles School District"
};

//make the request to Graph
try{
	let res = await client.api('/education/schools/10002')
		.version('beta')
		.update({educationSchool : schools});
	console.log(res);
} catch (error) {
	throw error;
}

```