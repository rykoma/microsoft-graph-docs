
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const dataLabels = {
  position: "position-value",
  showValue: true,
  showSeriesName: true,
  showCategoryName: true,
  showLegendKey: true
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/dataLabels')
		.update({workbookChartDataLabels : dataLabels});
	console.log(res);
} catch (error) {
	throw error;
}

```