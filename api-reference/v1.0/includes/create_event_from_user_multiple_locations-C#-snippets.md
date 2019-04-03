
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var displayName = "Home Office";

var coordinates = new OutlookGeoCoordinates
{
	Latitude = 47.672,
	Longitude = -102.103,
};

var address = new PhysicalAddress
{
	Street = "4567 Main St",
	City = "Redmond",
	State = "WA",
	CountryOrRegion = "US",
	PostalCode = "32008",
};

var displayNameVar = "Fourth Coffee";

var displayNameVarVar = "Conf Room 3";

var locations = new List<Location>();
locations.Add(new Location(displayNameVarVar));
locations.Add(new Location(displayNameVar,address,coordinates));
locations.Add(new Location(displayName));

var location = new Location
{
	DisplayName = "Conf Room 3; Fourth Coffee; Home Office",
	LocationType = "Default",
};

var type = "Required";

var emailAddress = new EmailAddress
{
	Address = "AlexW@contoso.onmicrosoft.com",
	Name = "Alex Wilber",
};

var typeVar = "Required";

var emailAddressVar = new EmailAddress
{
	Address = "DanaS@contoso.onmicrosoft.com",
	Name = "Dana Swope",
};

var attendees = new List<Attendee>();
attendees.Add(new Attendee(emailAddressVar,typeVar));
attendees.Add(new Attendee(emailAddress,type));

var end = new DateTimeTimeZone
{
	DateTime = "2017-08-30T12:00:00",
	TimeZone = "Pacific Standard Time",
};

var start = new DateTimeTimeZone
{
	DateTime = "2017-08-30T11:00:00",
	TimeZone = "Pacific Standard Time",
};

var body = new ItemBody
{
	ContentType = "HTML",
	Content = "Let's kick-start this event planning!",
};

var event = new Event
{
	Subject = "Plan summer company picnic",
	Body = body,
	Start = start,
	End = end,
	Attendees = attendees,
	Location = location,
	Locations = locations,
};

await graphClient.Me.Events
	.Request()
	.AddAsync(event);

```