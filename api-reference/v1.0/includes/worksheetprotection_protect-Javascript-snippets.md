
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const protect = {
  options: {
    allowFormatCells: true,
    allowFormatColumns: true,
    allowFormatRows: true,
    allowInsertColumns: true,
    allowInsertRows: true,
    allowInsertHyperlinks: true,
    allowDeleteColumns: true,
    allowDeleteRows: true,
    allowSort: true,
    allowAutoFilter: true,
    allowPivotTables: true
  }
}
;

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/protection/protect')
		.post({workbookWorksheetProtectionOptions : protect});
	console.log(res);
} catch (error) {
	throw error;
}

```