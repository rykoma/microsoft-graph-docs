
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const classes = {
  description: "Health Level 1",
  classCode: "Health 501",
  displayName: "Health 1",
  externalId: "11019",
  externalName: "Health Level 1",
  externalSource: "sis",
  mailNickname: "fineartschool.net"
};

//make the request to Graph
try{
	let res = await client.api('/education/classes')
		.post({educationClass : classes});
	console.log(res);
} catch (error) {
	throw error;
}

```