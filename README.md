# EJS Documentation Template
An EJS template for creating good looking API documentation from a JSON file.

## Usage
This template should be pre-rendered and served statically. When rendering, pass the JSON data down like this:
```js
ejs.renderFile('documentation.ejs', { ...data }, {}, (err, str) => {})
```

## Example JSON Input
```json
{
	"applicationName": "Example Application",
	"api": {
		"Category 1": {
			"description": "Category 1 Description",
			"/api/category1/test": {
				"name": "Test",
				"private": false,
				"method": "POST",
				"notes": [
					"Will move to /api/category1/testing soon!"
				],
				"description": "Test Endpoint",
				"parameters": [
					{
						"name": "query",
						"type": "string",
						"description": "Test Parameter (optional)"
					}
				],
				"example": "fetch('/api/category1/test', {\n    method: 'POST'\n})",
				"responses": [
					{
						"code": "200",
						"description": "Operation performed successfully."
					}
				]
			}
		}
	}
}
```

## Sample
You can view a sample JSON file and its rendered HTML in the `example` folder.

## Note
This template works best if you pre-render the EJS into an HTML file which you can then statically serve.

## License
[MIT](https://choosealicense.com/licenses/mit/)