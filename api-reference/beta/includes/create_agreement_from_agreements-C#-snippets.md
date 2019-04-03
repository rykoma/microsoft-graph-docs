
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var fileData = new AgreementFileData
{
	Data = "SGVsbG8gd29ybGQ=",
};

var isDefault = True;

var language = "en";

var fileName = "TOU.pdf";

var files = new List<AgreementFile>();
files.Add(new AgreementFile(fileName,language,isDefault,fileData));

var agreement = new Agreement
{
	DisplayName = "MSGraph Sample",
	IsViewingBeforeAcceptanceRequired = true,
	Files = files,
};

await graphClient.Agreements
	.Request()
	.AddAsync(agreement);

```