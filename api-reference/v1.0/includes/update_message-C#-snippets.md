
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of ItemBody
var body = new ItemBody
{
	ContentType = "",
	Content = "content-value",
};

//create instance of Message
var messages = new Message
{
	Subject = "subject-value",
	Body = body,
	InferenceClassification = "other",
};

await graphClient.Me.Messages["{id}"]
	.Request()
	.UpdateAsync(messages);

```