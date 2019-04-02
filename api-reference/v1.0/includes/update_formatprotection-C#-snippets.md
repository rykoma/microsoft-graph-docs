
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookFormatProtection
var protection = new WorkbookFormatProtection
{
	Locked = true,
	FormulaHidden = true,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"].Range().Format.Protection
	.Request()
	.UpdateAsync(protection);

```