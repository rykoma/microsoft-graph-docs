
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create NumberFormat list and populate it
var numberFormat = new List<NumberFormat>();

//create Formula list and populate it
var formula = new List<Formula>();

//create Values list and populate it
var values = new List<Values>();

//create instance of String
var range = new String
{
	Values = values,
	Formula = formula,
	NumberFormat = numberFormat,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{sheet-id}"].Range('A1:B2')
	.Request()
	.UpdateAsync(range);

```