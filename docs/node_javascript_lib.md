# Getting started

This is an example of a simple API for a "notes" service

## How to Build

The generated SDK relies on [Node Package Manager](https://www.npmjs.com/) (NPM) being available to resolve dependencies. If you don't already have NPM installed, please go ahead and follow instructions to install NPM from [here](https://nodejs.org/en/download/).
The SDK also requires Node to be installed. If Node isn't already installed, please install it from [here](https://nodejs.org/en/download/)
> NPM is installed by default when Node is installed

To check if node and npm have been successfully installed, write the following commands in command prompt:

* `node --version`
* `npm -version`

![Version Check](https://apidocs.io/illustration/nodejs?step=versionCheck&workspaceFolder=Notes%20Example%20API-Node)

Now use npm to resolve all dependencies by running the following command in the root directory (of the SDK folder):

```bash
npm install
```

![Resolve Dependencies](https://apidocs.io/illustration/nodejs?step=resolveDependency1&workspaceFolder=Notes%20Example%20API-Node)

![Resolve Dependencies](https://apidocs.io/illustration/nodejs?step=resolveDependency2)

This will install all dependencies in the `node_modules` folder.

Once dependencies are resolved, you will need to move the folder `NotesExampleAPILib ` in to your `node_modules` folder.

## How to Use

The following section explains how to use the library in a new project.

### 1. Open Project Folder
Open an IDE/Text Editor for JavaScript like Sublime Text. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

Click on `File` and select `Open Folder`.

![Open Folder](https://apidocs.io/illustration/nodejs?step=openFolder)

Select the folder of your SDK and click on `Select Folder` to open it up in Sublime Text. The folder will become visible in the bar on the left.

![Open Project](https://apidocs.io/illustration/nodejs?step=openProject&workspaceFolder=Notes%20Example%20API-Node)

### 2. Creating a Test File

Now right click on the folder name and select the `New File` option to create a new test file. Save it as `index.js` Now import the generated NodeJS library using the following lines of code:

```js
var lib = require('lib');
```

Save changes.

![Create new file](https://apidocs.io/illustration/nodejs?step=createNewFile&workspaceFolder=Notes%20Example%20API-Node)

![Save new file](https://apidocs.io/illustration/nodejs?step=saveNewFile&workspaceFolder=Notes%20Example%20API-Node)

### 3. Running The Test File

To run the `index.js` file, open up the command prompt and navigate to the Path where the SDK folder resides. Type the following command to run the file:

```
node index.js
```

![Run file](https://apidocs.io/illustration/nodejs?step=runProject&workspaceFolder=Notes%20Example%20API-Node)


## How to Test

These tests use Mocha framework for testing, coupled with Chai for assertions. These dependencies need to be installed for tests to run.
Tests can be run in a number of ways:

### Method 1 (Run all tests)

1. Navigate to the root directory of the SDK folder from command prompt.
2. Type `mocha --recursive` to run all the tests.

### Method 2 (Run all tests)

1. Navigate to the `../test/Controllers/` directory from command prompt.
2. Type `mocha *` to run all the tests.

### Method 3 (Run specific controller's tests)

1. Navigate to the `../test/Controllers/` directory from command prompt.
2. Type `mocha  Notes Example APIController`  to run all the tests in that controller file.

> To increase mocha's default timeout, you can change the `TEST_TIMEOUT` parameter's value in `TestBootstrap.js`.

![Run Tests](https://apidocs.io/illustration/nodejs?step=runTests&controllerName=Notes%20Example%20APIController)

## Initialization

### 

API client can be initialized as following:

```JavaScript
const lib = require('lib');


```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [NotesController](#notes_controller)

## <a name="notes_controller"></a>![Class: ](https://apidocs.io/img/class.png ".NotesController") NotesController

### Get singleton instance

The singleton instance of the ``` NotesController ``` class can be accessed from the API Client.

```javascript
var controller = lib.NotesController;
```

### <a name="get_notes"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.getNotes") getNotes

> List all notes, optionally filtered by a query string


```javascript
function getNotes(q, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| q |  ``` Optional ```  | An optional search query to filter the results |



#### Example Usage

```javascript

    var q = 'q';

    controller.getNotes(q, function(error, response, context) {

    
    });
```



### <a name="delete_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.deleteNotesById") deleteNotesById

> Remove the specified note


```javascript
function deleteNotesById(id, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |



#### Example Usage

```javascript

    var id = 2;

    controller.deleteNotesById(id, function(error, response, context) {

    
    });
```



### <a name="get_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.getNotesById") getNotesById

> Retrieve the specified note


```javascript
function getNotesById(id, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |



#### Example Usage

```javascript

    var id = 2;

    controller.getNotesById(id, function(error, response, context) {

    
    });
```



### <a name="update_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.updateNotesById") updateNotesById

> Update the specified note (allowing partial information)


```javascript
function updateNotesById(id, body, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var id = 70;
    var body = {
        id : 21
    };

    controller.updateNotesById(id, body, function(error, response, context) {

    
    });
```



### <a name="create_notes"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.createNotes") createNotes

> Create a new note in the collection


```javascript
function createNotes(body, xTrackingExample, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| xTrackingExample |  ``` Optional ```  | You can specify request headers like this |



#### Example Usage

```javascript

    var body = new NotesRequest({ "title": "Return sweater", "dueInDays": -2 });
    var xTrackingExample = new XTrackingExampleEnum(accounting);

    controller.createNotes(body, xTrackingExample, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)



