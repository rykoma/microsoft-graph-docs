
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var type = "required";

var emailAddress = new EmailAddress
{
	Address = "adelev@contoso.onmicrosoft.com",
	Name = "Adele Vance",
};

var attendees = new List<Attendee>();
attendees.Add(new Attendee(emailAddress,type));

var location = new Location
{
	DisplayName = "Harry's Bar",
};

var end = new DateTimeTimeZone
{
	DateTime = "2019-03-15T14:00:00",
	TimeZone = "Pacific Standard Time",
};

var start = new DateTimeTimeZone
{
	DateTime = "2019-03-15T12:00:00",
	TimeZone = "Pacific Standard Time",
};

var body = new ItemBody
{
	ContentType = "HTML",
	Content = "Does mid month work for you?",
};

var event = new Event
{
	Subject = "Let's go for lunch",
	Body = body,
	Start = start,
	End = end,
	Location = location,
	Attendees = attendees,
};

await graphClient.Me.Calendars["AAMkAGViNDU7zAAAAAGtlAAA="].Events
	.Request()
	.AddAsync(event);

```