
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of EmailAddress
var senderEmailAddress = new EmailAddress
{
	Name = "Samantha Booth",
	Address = "samanthab@adatum.onmicrosoft.com",
};

//create instance of InferenceClassificationOverride
var overrides = new InferenceClassificationOverride
{
	ClassifyAs = "focused",
	SenderEmailAddress = senderEmailAddress,
};

await graphClient.Me.InferenceClassification.Overrides
	.Request()
	.AddAsync(overrides);

```