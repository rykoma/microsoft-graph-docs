
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var bookingAppointment = await graphClient.BookingBusinesses["Contosolunchdelivery@M365B489948.onmicrosoft.com"].CalendarView
	.Request()
	.GetAsync();

```