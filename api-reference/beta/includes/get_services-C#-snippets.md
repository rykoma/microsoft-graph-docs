
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var bookingService = await graphClient.BookingBusinesses["Contosolunchdelivery@M365B489948.onmicrosoft.com"].Services
	.Request()
	.GetAsync();

```