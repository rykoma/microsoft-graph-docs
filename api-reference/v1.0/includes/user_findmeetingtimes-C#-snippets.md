
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of EmailAddress
var emailAddress = new EmailAddress
{
	Name = "Alex Wilbur",
	Address = "alexw@contoso.onmicrosoft.com",
};

var type = "required";

//create AttendeeBase list and populate it
var attendees = new List<AttendeeBase>();
attendees.Add(new AttendeeBase(type,emailAddress));

var displayName = "Conf room Hood";

var resolveAvailability = "false";

//create Locations list and populate it
var locations = new List<Locations>();
locations.Add(new Locations(resolveAvailability,displayName));

//create instance of AttendeeBase
var locationConstraint = new AttendeeBase
{
	IsRequired = "false",
	SuggestLocation = "false",
	Locations = locations,
};

//create instance of Timeslots
var end = new Timeslots
{
	DateTime = "2019-04-18T17:00:00",
	TimeZone = "Pacific Standard Time",
};

//create instance of Timeslots
var start = new Timeslots
{
	DateTime = "2019-04-16T09:00:00",
	TimeZone = "Pacific Standard Time",
};

//create Timeslots list and populate it
var timeslots = new List<Timeslots>();
timeslots.Add(new Timeslots(start,end));

//create instance of AttendeeBase
var timeConstraint = new AttendeeBase
{
	ActivityDomain = "work",
	Timeslots = timeslots,
};

var isOrganizerOptional = "false";

var meetingDuration = "PT1H";

var returnSuggestionReasons = "true";

var minimumAttendeePercentage = "100";

await graphClient.Me
	.FindMeetingTimes(attendees,locationConstraint,timeConstraint,meetingDuration,maxCandidates,isOrganizerOptional,returnSuggestionReasons,minimumAttendeePercentage)
	.Request()
	.PostAsync()

```