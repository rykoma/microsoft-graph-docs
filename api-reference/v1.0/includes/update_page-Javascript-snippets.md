
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const content = [
   {
    'target':'#para-id',
    'action':'insert',
    'position':'before',
    'content':'<img src="image-url-or-part-name" alt="image-alt-text" />'
  }, 
  {
    'target':'#list-id',
    'action':'append',
    'content':'<li>new-page-content</li>'
  }
];

//make the request to Graph
try{
	let res = await client.api('/me/onenote/pages/{id}/content')
		.update({Stream : content});
	console.log(res);
} catch (error) {
	throw error;
}

```