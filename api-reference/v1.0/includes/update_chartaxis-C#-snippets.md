
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Json
var minimum = new Json
{
};

//create instance of Json
var maximum = new Json
{
};

//create instance of Json
var majorUnit = new Json
{
};

//create instance of WorkbookChartAxis
var valueAxis = new WorkbookChartAxis
{
	MajorUnit = majorUnit,
	Maximum = maximum,
	Minimum = minimum,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].Axes.ValueAxis
	.Request()
	.UpdateAsync(valueAxis);

```