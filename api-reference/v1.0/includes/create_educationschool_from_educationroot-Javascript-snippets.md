
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const schools = {
  displayName: "Fabrikam High School",
  description: "Magnate school for the arts. Los Angeles School District",
  status: "String",
  externalSource: "String",
  principalEmail: "AmyR@fabrikam.com",
  principalName: "Amy Roebuck",
  externalPrincipalId: "14007",
  highestGrade: "12",
  lowestGrade: "9",
  schoolNumber: "10002",
  address: {
    city: "Los Angeles",
    countryOrRegion: "United States",
    postalCode: "98055",
    state: "CA",
    street: "12345 Main St."
  },
  externalId: "10002",
  fax: "+1 (253) 555-0101",
  phone: "+1 (253) 555-0102",
};

//make the request to Graph
try{
	let res = await client.api('/education/schools')
		.post({educationSchool : schools});
	console.log(res);
} catch (error) {
	throw error;
}

```