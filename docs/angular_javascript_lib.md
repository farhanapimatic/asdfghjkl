# Getting started

This is an example of a simple API for a "notes" service

## How to Build

The generated SDK requires AngularJS framework to work. If you do not already have angular downloaded, please go ahead and do it from [here](https://angularjs.org/).
If any of your models have `Date` or `Datetime` type fields or your endpoints have `Date`/`Datetime` type response, you will need to download and link [angular-moment](https://cdnjs.cloudflare.com/ajax/libs/angular-moment/1.0.1/angular-moment.min.js) and [moment.js](https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.17.1/moment.min.js) with your project.

## How to Use

The following section describes how to use the generated SDK in an existing/new project.

### 1. Configure Angular and Generated SDK
Perform the following steps to configure angular and the SDK:
+ Make a `scripts` folder inside the root folder of the project. If you already have a `scripts` folder, skip to the next step.
+ Move the `angular.min.js` file inside the scripts folder. 
+ Move the `NotesExampleAPILib` folder inside the scripts folder.
+ If any of the Custom Types in your API have `Date`/`Datetime` type fields or any endpoint has `Date`/`Datetime` response, you will need to download angular-moment and moment.js. Move these 2 files into the `scripts` folder as well.

![folder-structure-image](https://apidocs.io/illustration/angularjs?step=folderStructure&workspaceFolder=Notes%20Example%20API-Angular&projectName=NotesExampleAPILib)

### 2. Open Project Folder
Open an IDE/Text Editor for JavaScript like Sublime Text. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.  
Click on `File` and select `Open Folder`

Select the folder of your SDK and click on `Select Folder` to open it up in Sublime Text. The folder will become visible in the bar on the left.

![open-folder-image](https://apidocs.io/illustration/angularjs?step=openFolder&workspaceFolder=Notes%20Example%20API-Angular)

### 3. Create an Angular Application
Since Angular JS is used for client-side web development, in order to use the generated library, you will have to develop an application first.
If you already have an angular application, [skip to Step 6](#6-include-sdk-references-in-html-file). Otherwise, follow these steps to create one:

+ In the IDE, click on `File` and choose `New File` to create a new file.
+ Add the following starting code in the file:
```js
var app = angular.module('myApp', []);
app.controller('testController', function($scope) 
{

});
```
+ Save it with the name `app.js` in the `scripts` folder.


### 4. Create HTML File
Skip to the next step if you are working with an existing project and already have an html file. Otherwise follow the steps to create one:
+ Inside the IDE, right click on the project folder name and select the `New File` option to create a new test file.
+ Save it with an appropriate name such as `index.html` in the root of your project folder.
`index.html` should look like this:
```html
<!DOCTYPE html>
<html>
<head>
	<title>Angular Project</title>
	<script></script>
</head>

<body>
</body>

</html>
```

![initial-html-code-image](https://apidocs.io/illustration/angularjs?step=initialCode&workspaceFolder=Notes%20Example%20API-Angular)

### 5. Including links to Angular in HTML file
Your HTML file needs to have a link to `angular.min.js` file to use Angular-JS. Add the link using `script` tags inside the `head` section of `index.html` like:
```html
<script src="scripts/angular.min.js" ></script>
```
If any of the Custom Types that you have defined have `Date`/`Datetime` type fields or any endpoint has `Date`/`Datetime` response, you will also need to link to angular-moment and moment.js like:
```html
<script src="scripts/angular.min.js" ></script>
<script src="scripts/moment.min.js" ></script>
<script src="scripts/angular-moment.min.js" ></script>
```

### 6. Include SDK references in HTML file
Import the reference to the generated SDK files inside your html file like:
```html
<head>
    ...
    <!-- Helper files -->
    <script src="scripts/NotesExampleAPILib/Module.js"></script>
    <script src="scripts/NotesExampleAPILib/Configuration.js"></script>
    <script src="scripts/NotesExampleAPILib/ModelFactory.js"></script>
    <script src="scripts/NotesExampleAPILib/ObjectMapper.js"></script>
    <script src="scripts/NotesExampleAPILib/APIHelper.js"></script>
    <script src="scripts/NotesExampleAPILib/Http/Client/HttpContext.js"></script>
    <script src="scripts/NotesExampleAPILib/Http/Client/RequestClient.js"></script>
    <script src="scripts/NotesExampleAPILib/Http/Request/HttpRequest.js"></script>
    <script src="scripts/NotesExampleAPILib/Http/Response/HttpResponse.js"></script>

    <!-- API Controllers -->
    <script src="scripts/NotesExampleAPILib/Controllers/BaseController.js"></script>
    <script src="scripts/NotesExampleAPILib/Controllers/NotesController.js"></script>


    <!-- Models -->
    <script src="scripts/NotesExampleAPILib/Models/BaseModel.js"></script>
    <script src="scripts/NotesExampleAPILib/Models/NotesRequest.js"></script>
    <script src="scripts/NotesExampleAPILib/Models/XTrackingExampleEnum.js"></script>
    <script src="scripts/NotesExampleAPILib/Models/NotesResponse.js"></script>
    <script src="scripts/NotesExampleAPILib/Models/MObject.js"></script>

    ...
</head>
```
> The `Module.js` file should be imported before the other files. After `Module.js`, `Configuration.js` should be imported.
> The `ModelFactory.js` file is needed by `ObjectMapper.js` file. The `ObjectMapper` in turn, is needed by `BaseController.js`.

### 7. Including link to `app.js` in HTML file
Link your `app.js` file to your `index.html` file like:
```html
<head>
	...
	<script src="scripts/app.js"></script>
</head>
```
> The link to app.js needs to be included at the very end of the head tag, after the SDK references have been added

### 8. Initializing the Angular App
You need to initialize your app and the controller associated with your view inside your `index.html` file. Do so like:
+ Add ng-app directive to initialize your app inside the `body` tag.
```html
<body ng-app="myApp">
```
+ Add ng-controller directive to initialize your controller and bind it with your view (`index.html` file).
```html
...
<body ng-app="myApp">
	<div ng-controller="testController">
		...
	</div>
	...
</body>
...
```

### 9. Consuming the SDK 
In order to use the generated SDK's modules, controllers and factories, the project needs to be added as a dependency in your angular app's module. This will be done inside the `app.js` file.
Add the dependency like this:

```js
var app = angular.module('myApp', ['NotesExampleAPILib']);
```
At this point, the SDK has been successfully included in your project. Further steps include using a service/factory from the generated SDK. To see working example of this, please head on [over here](#list-of-controllers) and choose any class to see its functions and example usage.  

### 10. Running The App
To run the app, simply open up the `index.html` file in a browser.

![app-running](https://apidocs.io/illustration/angularjs?step=appRunning)

## Initialization


The Angular Application can be initialized as following:
```JavaScript
var app = angular.module('myApp', [NotesExampleAPILib]);
// now controllers/services can be created which import
// the factories provided by the sdk
```
### 




# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [NotesController](#notes_controller)

## <a name="notes_controller"></a>![Class: ](https://apidocs.io/img/class.png ".NotesController") NotesController

### Get singleton instance

The singleton instance of the ``` NotesController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, NotesController, NotesResponse){
	});
```

### <a name="get_notes"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.getNotes") getNotes

> List all notes, optionally filtered by a query string


```javascript
function getNotes(q)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| q |  ``` Optional ```  | An optional search query to filter the results |



#### Example Usage

```javascript


	app.controller("testController", function($scope, NotesController, NotesResponse){
        var q = 'q';


		var result = NotesController.getNotes(q);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="delete_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.deleteNotesById") deleteNotesById

> Remove the specified note


```javascript
function deleteNotesById(id)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |



#### Example Usage

```javascript


	app.controller("testController", function($scope, NotesController){
        var id = 2;


		var result = NotesController.deleteNotesById(id);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.getNotesById") getNotesById

> Retrieve the specified note


```javascript
function getNotesById(id)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |



#### Example Usage

```javascript


	app.controller("testController", function($scope, NotesController, NotesResponse){
        var id = 2;


		var result = NotesController.getNotesById(id);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="update_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.updateNotesById") updateNotesById

> Update the specified note (allowing partial information)


```javascript
function updateNotesById(id, body)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, NotesController, NotesResponse){
        var id = 248;
        var body = {
            id : 21
        };


		var result = NotesController.updateNotesById(id, body);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_notes"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.createNotes") createNotes

> Create a new note in the collection


```javascript
function createNotes(body, xTrackingExample)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| xTrackingExample |  ``` Optional ```  | You can specify request headers like this |



#### Example Usage

```javascript


	app.controller("testController", function($scope, NotesController, NotesResponse){
        var body = new NotesRequest({ "title": "Return sweater", "dueInDays": -2 });
        var xTrackingExample = new XTrackingExampleEnum|null(accounting);


		var result = NotesController.createNotes(body, xTrackingExample);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)



