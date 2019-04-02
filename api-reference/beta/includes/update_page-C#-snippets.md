
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var content = "<li>new-page-content</li>";

var action = "append";

var target = "#list-id";

var contentVar = "<img src="image-url-or-part-name" alt="image-alt-text" />";

var position = "before";

var actionVar = "insert";

var targetVar = "#para-id";

//create Stream list and populate it
var contentVarVar = new List<Stream>();
contentVar.Add(new Stream(targetVar,actionVar,position,contentVar));
content.Add(new Stream(target,action,content));

await graphClient.Me.Onenote.Pages["{id}"].Content
	.Request()
	.UpdateAsync(content);

```