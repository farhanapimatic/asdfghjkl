# Getting started

This is an example of a simple API for a "notes" service

## How to Build

The generated code uses a few Gradle dependencies e.g., Jackson, Volley,
and Apache HttpClient. The reference to these dependencies is already
added in the build.gradle file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Android Studio click on ``` Open an Existing Android Project ```.

![Importing SDK into Android Studio - Step 1](https://apidocs.io/illustration/android?step=import1&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

* Browse to locate the folder containing the source code. Select the location of the NotesExampleAPI gradle project and click ``` Ok ```.

![Importing SDK into Android Studio - Step 2](https://apidocs.io/illustration/android?step=import2&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

* Upon successful import, the project can be built by clicking on ``` Build > Make Project ``` or  pressing ``` Ctrl + F9 ```.

![Importing SDK into Android Studio - Step 3](https://apidocs.io/illustration/android?step=import3&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

## How to Use

The following section explains how to use the NotesExampleAPI library in a new project.

### 1. Starting a new project 

For starting a new project, click on ``` Create New Android Studio Project ```.

![Add a new project in Android Studio - Step 1](https://apidocs.io/illustration/android?step=createNewProject0&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

Here, configure the new project by adding the name, domain and location of the sample application followed by clicking ``` Next ```.

![Create a new Android Studio Project - Step 2](https://apidocs.io/illustration/android?step=createNewProject1&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

Following this, select the `Phone and Tablet` option as shown in the illustration below and click `Next`.

![Create a new Android Studio Project - Step 3](https://apidocs.io/illustration/android?step=createNewProject2&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

In the following step, choose ``` Empty Activity ``` as the activity type and click ``` Next ```.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject3&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

In this step, provide an ``` Activity Name ``` and ``` Layout Name ``` and click ``` Finish ```.  This would take you to the newly created project.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject4&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

### 2. Add reference of the library project

In order to add a dependency to this sample application, click on the android button shown in the project explorer on the left side as shown in the picture. Click on ``` Project ``` in the drop down that emerges.  

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/android?step=testProject0&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

Right click the sample application in the project explorer and click on ``` New > Module ```  as shown in the picture.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/android?step=testProject1&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

Choose ``` Import Gradle Project ``` and click ``` Next ```.

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/android?step=testProject2&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

Click on ``` Finish ``` which would take you back to the sample application with the refernced SDK. 

![Adding dependency to the client library - Step 4](https://apidocs.io/illustration/android?step=testProject3&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

In the following step naigate to the ``` SampleApplication >  app > build.gradle ``` file and add the following line ```compile project(path: ':NotesExampleAPI')``` to the dependencies section as shown in the illustration below.

![Adding dependency to the client library - Step 5](https://apidocs.io/illustration/android?step=testProject4&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

Finally, press ``` Sync Now ``` in the warning visible as shown in the picture below.

![Adding dependency to the client library - Step 6](https://apidocs.io/illustration/android?step=testProject5&workspaceFolder=Notes%20Example%20API&workspaceName=NotesExampleAPI&projectName=NotesExampleAPILib&rootNamespace=com.example)

### 3. Write sample code

Once the ``` SampleApplication ``` is created, a file named ``` SampleApplication > app > src > main > java > MainActivity ``` will be visible in the *Project Explorer* with an ``` onCreate ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Android Studio, for running the tests do the following:

1. Right click on *SampleApplication > NotesExampleAPILib > androidTest > java)* from the project explorer.
2. Select "Run All Tests" or use "Ctrl + Shift + F10" to run the Tests.

## Initialization

### 

API client can be initialized as following. The `appContext` being passed is the Android application [`Context`](https://developer.android.com/reference/android/content/Context.html).

```java

com.example.Configuration.initialize(appContext);
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
    int id = 69;
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



