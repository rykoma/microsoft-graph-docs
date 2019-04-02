
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create Threads list and populate it
var topPicks = new List<Threads>();

var expirationDate = 8/3/2016 11:00:00 AM;

var companyName = "Contoso";

var extensionName = "Com.Contoso.Benefits";

var @odata.type = "Microsoft.OutlookServices.OpenTypeExtension";

//create Threads list and populate it
var Extensions = new List<Threads>();
Extensions.Add(new Threads(@odata.type,extensionName,companyName,expirationDate,topPicks));

//create instance of Threads
var Body = new Threads
{
	ContentType = "HTML",
	Content = "This is urgent!",
};

//create Threads list and populate it
var Posts = new List<Threads>();
Posts.Add(new Threads(Body,Extensions));

//create Threads list and populate it
var Threads = new List<Threads>();
Threads.Add(new Threads(Posts));

//create instance of Conversation
var conversations = new Conversation
{
	Topic = "Does anyone have a second?",
	Threads = Threads,
};

await graphClient.Groups["37df2ff0-0de0-4c33-8aee-75289364aef6"].Conversations
	.Request()
	.AddAsync(conversations);

```