# Getting started

This is an example of a simple API for a "notes" service

## How to Build

The generated code uses a few Maven dependencies e.g., Jackson, UniRest,
and Apache HttpClient. The reference to these dependencies is already
added in the pom.xml file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Eclipse click on ``` File -> Import ```.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/java?step=import0&workspaceFolder=Notes%20Example%20API-Java&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

* In the import dialog, select ``` Existing Java Project ``` and click ``` Next ```.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/java?step=import1&workspaceFolder=Notes%20Example%20API-Java&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

* Browse to locate the folder containing the source code. Select the detected location of the project and click ``` Finish ```.

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/java?step=import2&workspaceFolder=Notes%20Example%20API-Java&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

* Upon successful import, the project will be automatically built by Eclipse after automatically resolving the dependencies.

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/java?step=import3&workspaceFolder=Notes%20Example%20API-Java&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

## How to Use

The following section explains how to use the NotesExampleAPI library in a new console project.

### 1. Starting a new project

For starting a new project, click the menu command ``` File > New > Project ```.

![Add a new project in Eclipse](https://apidocs.io/illustration/java?step=createNewProject0&workspaceFolder=Notes%20Example%20API-Java&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

Next, choose ``` Maven > Maven Project ```and click ``` Next ```.

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/java?step=createNewProject1&workspaceFolder=Notes%20Example%20API-Java&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

Here, make sure to use the current workspace by choosing ``` Use default Workspace location ```, as shown in the picture below and click ``` Next ```.

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/java?step=createNewProject2&workspaceFolder=Notes%20Example%20API-Java&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

Following this, select the *quick start* project type to create a simple project with an existing class and a ``` main ``` method. To do this, choose ``` maven-archetype-quickstart ``` item from the list and click ``` Next ```.

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/java?step=createNewProject3&workspaceFolder=Notes%20Example%20API-Java&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

In the last step, provide a ``` Group Id ``` and ``` Artifact Id ``` as shown in the picture below and click ``` Finish ```.

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/java?step=createNewProject4&workspaceFolder=Notes%20Example%20API-Java&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

### 2. Add reference of the library project

The created Maven project manages its dependencies using its ``` pom.xml ``` file. In order to add a dependency on the *NotesExampleAPILib* client library, double click on the ``` pom.xml ``` file in the ``` Package Explorer ```. Opening the ``` pom.xml ``` file will render a graphical view on the cavas. Here, switch to the ``` Dependencies ``` tab and click the ``` Add ``` button as shown in the picture below.

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/java?step=testProject0&workspaceFolder=Notes%20Example%20API-Java&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

Clicking the ``` Add ``` button will open a dialog where you need to specify NotesExampleAPI in ``` Group Id ``` and NotesExampleAPILib in the ``` Artifact Id ``` fields. Once added click ``` OK ```. Save the ``` pom.xml ``` file.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?step=testProject1&workspaceFolder=Notes%20Example%20API-Java&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

### 3. Write sample code

Once the ``` SimpleConsoleApp ``` is created, a file named ``` App.java ``` will be visible in the *Package Explorer* with a ``` main ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?step=testProject2&workspaceFolder=Notes%20Example%20API-Java&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Eclipse, for running the tests do the following:

1. Select the project *NotesExampleAPILib* from the package explorer.
2. Select "Run -> Run as -> JUnit Test" or use "Alt + Shift + X" followed by "T" to run the Tests.

## Initialization

### 

API client can be initialized as following.

```java

NotesExampleAPIClient client = new NotesExampleAPIClient();
```


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [NotesController](#notes_controller)

## <a name="notes_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.NotesController") NotesController

### Get singleton instance

The singleton instance of the ``` NotesController ``` class can be accessed from the API Client.

```java
NotesController notes = client.getNotes();
```

### <a name="get_notes_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.NotesController.getNotesAsync") getNotesAsync

> List all notes, optionally filtered by a query string


```java
void getNotesAsync(
        final String q,
        final APICallBack<List<NotesResponse>> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| q |  ``` Optional ```  | An optional search query to filter the results |


#### Example Usage

```java
String q = "q";
// Invoking the API call with sample inputs
notes.getNotesAsync(q, new APICallBack<List<NotesResponse>>() {
    public void onSuccess(HttpContext context, List<NotesResponse> response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="delete_notes_by_id_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.NotesController.deleteNotesByIdAsync") deleteNotesByIdAsync

> Remove the specified note


```java
void deleteNotesByIdAsync(
        final int id,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |


#### Example Usage

```java
int id = 2;
// Invoking the API call with sample inputs
notes.deleteNotesByIdAsync(id, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="get_notes_by_id_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.NotesController.getNotesByIdAsync") getNotesByIdAsync

> Retrieve the specified note


```java
void getNotesByIdAsync(
        final int id,
        final APICallBack<NotesResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |


#### Example Usage

```java
int id = 2;
// Invoking the API call with sample inputs
notes.getNotesByIdAsync(id, new APICallBack<NotesResponse>() {
    public void onSuccess(HttpContext context, NotesResponse response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="update_notes_by_id_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.NotesController.updateNotesByIdAsync") updateNotesByIdAsync

> Update the specified note (allowing partial information)


```java
void updateNotesByIdAsync(
        final int id,
        final Object body,
        final APICallBack<NotesResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    int id = 161;
    Object body = new Object();
    // Invoking the API call with sample inputs
    notes.updateNotesByIdAsync(id, body, new APICallBack<NotesResponse>() {
        public void onSuccess(HttpContext context, NotesResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="create_notes_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.NotesController.createNotesAsync") createNotesAsync

> Create a new note in the collection


```java
void createNotesAsync(
        final NotesRequest body,
        final XTrackingExampleEnum xTrackingExample,
        final APICallBack<NotesResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| xTrackingExample |  ``` Optional ```  | You can specify request headers like this |


#### Example Usage

```java
try {
    String bodyValue = "{ \"title\": \"Return sweater\", \"dueInDays\": -2 }";
    NotesRequest body = mapper.readValue(bodyValue,new TypeReference<NotesRequest> (){});
    XTrackingExampleEnum xTrackingExample = XTrackingExampleEnum.fromString("accounting");
    // Invoking the API call with sample inputs
    notes.createNotesAsync(body, xTrackingExample, new APICallBack<NotesResponse>() {
        public void onSuccess(HttpContext context, NotesResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)



