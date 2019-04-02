
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const schemaExtensions = {
    id:"courses",
    description: "Graph Learn training courses extensions",
    targetTypes: [
        "Group"
    ],
    properties: [
        {
            name: "courseId",
            type: "Integer"
        },
        {
            name: "courseName",
            type: "String"
        },
        {
            name: "courseType",
            type: "String"
        }
    ]
}
;

//make the request to Graph
try{
	let res = await client.api('/schemaExtensions')
		.post({schemaExtension : schemaExtensions});
	console.log(res);
} catch (error) {
	throw error;
}

```