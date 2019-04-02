
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of AccessReview
var accessReviews = new AccessReview
{
	DisplayName = "TestReview new name",
};

await graphClient.AccessReviews["006111db-0810-4494-a6df-904d368bd81b"]
	.Request()
	.UpdateAsync(accessReviews);

```