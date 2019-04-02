
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of D280ed1a-9f6b-4f9c-a962-fb4d00dc50ff
var d280ed1a-9f6b-4f9c-a962-fb4d00dc50ff = new D280ed1a-9f6b-4f9c-a962-fb4d00dc50ff
{
	@odata.type = "microsoft.graph.plannerChecklistItem",
	IsChecked = true,
};

//create instance of 95e27074-6c4a-447a-aa24-9d718a0b86fa
var 95e27074-6c4a-447a-aa24-9d718a0b86fa = new 95e27074-6c4a-447a-aa24-9d718a0b86fa
{
	@odata.type = "microsoft.graph.plannerChecklistItem",
	Title = "Update task details",
	IsChecked = true,
};

//create instance of PlannerChecklistItems
var checklist = new PlannerChecklistItems
{
	95e27074-6c4a-447a-aa24-9d718a0b86fa = 95e27074-6c4a-447a-aa24-9d718a0b86fa,
	D280ed1a-9f6b-4f9c-a962-fb4d00dc50ff = d280ed1a-9f6b-4f9c-a962-fb4d00dc50ff,
	A93c93c5-10a6-4167-9551-8bafa09967a7 = null,
};

//create instance of Https%3A//developer%2Emicrosoft%2Ecom/en-us/graph/graph-explorer
var https%3A//developer%2Emicrosoft%2Ecom/en-us/graph/graph-explorer = new Https%3A//developer%2Emicrosoft%2Ecom/en-us/graph/graph-explorer
{
	@odata.type = "microsoft.graph.plannerExternalReference",
	PreviewPriority = "  !!",
};

//create instance of Http%3A//developer%2Emicrosoft%2Ecom
var http%3A//developer%2Emicrosoft%2Ecom = new Http%3A//developer%2Emicrosoft%2Ecom
{
	@odata.type = "microsoft.graph.plannerExternalReference",
	Alias = "Documentation",
	PreviewPriority = " !",
	Type = "Other",
};

//create instance of PlannerExternalReferences
var references = new PlannerExternalReferences
{
	Http%3A//developer%2Emicrosoft%2Ecom = http%3A//developer%2Emicrosoft%2Ecom,
	Https%3A//developer%2Emicrosoft%2Ecom/en-us/graph/graph-explorer = https%3A//developer%2Emicrosoft%2Ecom/en-us/graph/graph-explorer,
	Http%3A//www%2Ebing%2Ecom = null,
};

//create instance of PlannerTaskDetails
var details = new PlannerTaskDetails
{
	PreviewType = "noPreview",
	References = references,
	Checklist = checklist,
};

await graphClient.Planner.Tasks["gcrYAaAkgU2EQUvpkNNXLGQAGTtu"].Details
	.Request()
	.UpdateAsync(details);

```