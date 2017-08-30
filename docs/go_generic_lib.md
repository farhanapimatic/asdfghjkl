# Getting started

This is an example of a simple API for a "notes" service

## How to Build


* In order to successfully build and run your SDK files, you are required to have the following setup in your system:
    * **Go**  (Visit [https://golang.org/doc/install](https://golang.org/doc/install) for more details on how to install Go)
    * **Java VM** Version 8 or later
    * **Eclipse 4.6 (Neon)** or later ([http://www.eclipse.org/neon/](http://www.eclipse.org/neon/))
    * **GoClipse** setup within above installed Eclipse (Follow the instructions at [this link](https://github.com/GoClipse/goclipse/blob/latest/documentation/Installation.md#instructions) to setup GoClipse)
* Ensure that ```GOPATH``` environment variable is set in the system variables. If not, set it to your workspace directory where you will be adding your Go projects.
* The generated code uses unirest-go http library. Therefore, you will need internet access to resolve this dependency. If Go is properly installed and configured, run the following command to pull the dependency:

```Go
go get github.com/apimatic/unirest-go
```

This will install unirest-go in the ```GOPATH``` you specified in the system variables.

Now follow the steps mentioned below to build your SDK:

1. Open eclipse in the Go language perspective and click on the ```Import``` option in ```File``` menu.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/go?step=import0)

2. Select ```General -> Existing Projects into Workspace``` option from the tree list.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/go?step=import1)

3. In ```Select root directory```, provide path to the unzipped archive for the generated code. Once the path is set and the Project becomes visible under ```Projects``` click ```Finish```

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/go?step=import2&workspaceFolder=Notes%20Example%20API-GoLang&projectName=notesexampleapi_lib)

4. The Go library will be imported and its files will be visible in the Project Explorer

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/go?step=import3&projectName=notesexampleapi_lib)

## How to Use

The following section explains how to use the NotesexampleapiLib library in a new project.

### 1. Add a new Test Project

Create a new project in Eclipse by ```File``` -> ```New``` -> ```Go Project```

![Add a new project in Eclipse](https://apidocs.io/illustration/go?step=createNewProject0)

Name the Project as ```Test``` and click ```Finish```

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/go?step=createNewProject1)

Create a new directory in the ```src``` directory of this project

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/go?step=createNewProject2&projectName=notesexampleapi_lib)

Name it ```test.com```

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/go?step=createNewProject3&projectName=notesexampleapi_lib)

Now create a new file inside ```src/test.com```

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/go?step=createNewProject4&projectName=notesexampleapi_lib)

Name it ```testsdk.go```

![Create a new Maven Project - Step 5](https://apidocs.io/illustration/go?step=createNewProject5&projectName=notesexampleapi_lib)

In this Go file, you can start adding code to initialize the client library. Sample code to initialize the client library and using its methods is given in the subsequent sections.

### 2. Configure the Test Project

You need to import your generated library in this project in order to make use of its functions. In order to import the library, you can add its path in the ```GOPATH``` for this project. Follow the below steps:

Right click on the project name and click on ```Properties```

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/go?step=testProject0&projectName=notesexampleapi_lib)

Choose ```Go Compiler``` from the side menu. Check ```Use project specific settings``` and uncheck ```Use same value as the GOPATH environment variable.```. By default, the GOPATH value from the environment variables will be visible in ```Eclipse GOPATH```. Do not remove this as this points to the unirest dependency.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/go?step=testProject1)

Append the library path to this GOPATH

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/go?step=testProject2&workspaceFolder=Notes%20Example%20API-GoLang)

Once the path is appended, click on ```OK```

### 3. Build the Test Project

Right click on the project name and click on ```Build Project```

![Build Project](https://apidocs.io/illustration/go?step=buildProject&projectName=notesexampleapi_lib)

### 4. Run the Test Project

If the build is successful, right click on your Go file and click on ```Run As``` -> ```Go Application```

![Run Project](https://apidocs.io/illustration/go?step=runProject&projectName=notesexampleapi_lib)

# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [notes_pkg](#notes_pkg)

## <a name="notes_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".notes_pkg") notes_pkg

### Get instance

Factory for the ``` NOTES ``` interface can be accessed from the package notes_pkg.

```go
notes := notes_pkg.NewNOTES()
```

### <a name="get_notes"></a>![Method: ](https://apidocs.io/img/method.png ".notes_pkg.GetNotes") GetNotes

> List all notes, optionally filtered by a query string


```go
func (me *NOTES_IMPL) GetNotes(q *string)([]*models_pkg.NotesResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| q |  ``` Optional ```  | An optional search query to filter the results |


#### Example Usage

```go
q := "q"

var result []*models_pkg.NotesResponse
result,_ = notes.GetNotes(q)

```


### <a name="delete_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".notes_pkg.DeleteNotesById") DeleteNotesById

> Remove the specified note


```go
func (me *NOTES_IMPL) DeleteNotesById(id int64)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |


#### Example Usage

```go
id,_ := strconv.ParseInt("2", 10, 8)

var result 
result,_ = notes.DeleteNotesById(id)

```


### <a name="get_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".notes_pkg.GetNotesById") GetNotesById

> Retrieve the specified note


```go
func (me *NOTES_IMPL) GetNotesById(id int64)(*models_pkg.NotesResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |


#### Example Usage

```go
id,_ := strconv.ParseInt("2", 10, 8)

var result *models_pkg.NotesResponse
result,_ = notes.GetNotesById(id)

```


### <a name="update_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".notes_pkg.UpdateNotesById") UpdateNotesById

> Update the specified note (allowing partial information)


```go
func (me *NOTES_IMPL) UpdateNotesById(
            id int64,
            body interface{})(*models_pkg.NotesResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
id,_ := strconv.ParseInt("111", 10, 8)
var body interface{}

var result *models_pkg.NotesResponse
result,_ = notes.UpdateNotesById(id, body)

```


### <a name="create_notes"></a>![Method: ](https://apidocs.io/img/method.png ".notes_pkg.CreateNotes") CreateNotes

> Create a new note in the collection


```go
func (me *NOTES_IMPL) CreateNotes(
            body *models_pkg.NotesRequest,
            xTrackingExample models_pkg.XTrackingExampleEnum)(*models_pkg.NotesResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| xTrackingExample |  ``` Optional ```  | You can specify request headers like this |


#### Example Usage

```go
bodyValue := []byte("{ \"title\": \"Return sweater\", \"dueInDays\": -2 }")
var body *models_pkg.NotesRequest
json.Unmarshal(bodyValue,&body)
xTrackingExample := models_pkg.X-Tracking-ExampleEnum_ACCOUNTING

var result *models_pkg.NotesResponse
result,_ = notes.CreateNotes(body, xTrackingExample)

```


[Back to List of Controllers](#list_of_controllers)



