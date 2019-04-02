
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of InferenceClassificationOverride
var overrides = new InferenceClassificationOverride
{
	ClassifyAs = "focused",
};

await graphClient.Me.InferenceClassification.Overrides["{id}"]
	.Request()
	.UpdateAsync(overrides);

```