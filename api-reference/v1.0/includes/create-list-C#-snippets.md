
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var list = new ListInfo
{
	Template = "genericList",
};

var number = new NumberColumn
{
};

var name = "PageCount";

var text = new TextColumn
{
};

var nameVar = "Author";

var columns = new List<ColumnDefinition>();
columns.Add(new ColumnDefinition(nameVar,text));
columns.Add(new ColumnDefinition(name,number));

var listVar = new List
{
	Name = "Books",
	Columns = columns,
	List = list,
};

await graphClient.Sites["{site-id}"].Lists
	.Request()
	.AddAsync(list);

```