
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var staffMembers = await graphClient.BookingBusinesses["Contosolunchdelivery@M365B489948.onmicrosoft.com"].StaffMembers["71d64d0e-7225-49b6-b0b1-070d476cda51"]
	.Request()
	.GetAsync();

```