# Getting started

This is an example of a simple API for a "notes" service

## How to Build


The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```PodFile``` file that comes with the SDK. 
To resolve these dependencies, we use the Cocoapods package manager.
Visit https://guides.cocoapods.org/using/getting-started.html to setup Cocoapods on your system.
Open command prompt and type ```pod --version```. This should display the current version of Cocoapods installed if the installation was successful.

Using command line, navigate to the directory containing the generated files (including ```PodFile```) for the SDK. 
Run the command ```pod install```. This should install all the required dependencies and create the ```pods``` directory in your project directory.

![Installing dependencies using Cocoapods](https://apidocs.io/illustration/objc?step=AddDependencies&workspaceFolder=Notes%20Example%20API-ObjC&workspaceName=NotesExampleAPI&projectName=NotesExampleAPI&rootNamespace=NotesExampleAPI)

Open the project workspace using the (NotesExampleAPI.xcworkspace) file. Invoke the build process using `Command(⌘)+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Xcode](https://apidocs.io/illustration/objc?step=BuildSDK&workspaceFolder=Notes%20Example%20API-ObjC&workspaceName=NotesExampleAPI&projectName=NotesExampleAPI&rootNamespace=NotesExampleAPI)


## How to Use

The generated code is a Cocoa Touch Static Library which can be used in any iOS project. The support for these generated libraries go all the way back to iOS 6.

The following section explains how to use the NotesExampleAPI library in a new iOS project.     
### 1. Starting a new project
To start a new project, left-click on the ```Create a new Xcode project```.
![Create Test Project - Step 1](https://apidocs.io/illustration/objc?step=Test1&workspaceFolder=Notes%20Example%20API-ObjC&workspaceName=NotesExampleAPI&projectName=NotesExampleAPI&rootNamespace=NotesExampleAPI)

Next, choose **Single View Application** and click ```Next```.
![Create Test Project - Step 2](https://apidocs.io/illustration/objc?step=Test2&workspaceFolder=Notes%20Example%20API-ObjC&workspaceName=NotesExampleAPI&projectName=NotesExampleAPI&rootNamespace=NotesExampleAPI)

Provide **Test-Project** as the product name click ```Next```.
![Create Test Project - Step 3](https://apidocs.io/illustration/objc?step=Test3&workspaceFolder=Notes%20Example%20API-ObjC&workspaceName=NotesExampleAPI&projectName=NotesExampleAPI&rootNamespace=NotesExampleAPI)

Choose the desired location of your project folder and click ```Create```.
![Create Test Project - Step 4](https://apidocs.io/illustration/objc?step=Test4&workspaceFolder=Notes%20Example%20API-ObjC&workspaceName=NotesExampleAPI&projectName=NotesExampleAPI&rootNamespace=NotesExampleAPI)

### 2. Adding the static library dependency
To add this dependency open a terminal and navigate to your project folder. Next, input ```pod init``` and press enter.
![Add dependency - Step 1](https://apidocs.io/illustration/objc?step=Add0&workspaceFolder=Notes%20Example%20API-ObjC&workspaceName=NotesExampleAPI&projectName=NotesExampleAPI&rootNamespace=NotesExampleAPI)

Next, open the newly created ```PodFile``` in your favourite text editor. Add the following line : pod 'NotesExampleAPI', :path => 'Vendor/NotesExampleAPI'
![Add dependency - Step 2](https://apidocs.io/illustration/objc?step=Add1&workspaceFolder=Notes%20Example%20API-ObjC&workspaceName=NotesExampleAPI&projectName=NotesExampleAPI&rootNamespace=NotesExampleAPI)

Execute `pod install` from terminal to install the dependecy in your project. This would add the dependency to the newly created test project.
![Add dependency - Step 3](https://apidocs.io/illustration/objc?step=Add2&workspaceFolder=Notes%20Example%20API-ObjC&workspaceName=NotesExampleAPI&projectName=NotesExampleAPI&rootNamespace=NotesExampleAPI)


## How to Test

Unit tests in this SDK can be run using Xcode. 

First build the SDK as shown in the steps above and naivgate to the project directory and open the NotesExampleAPI.xcworkspace file.

Go to the test explorer in Xcode as shown in the picture below and click on `run tests` from the menu. 
![Run tests](https://apidocs.io/illustration/objc?step=RunTests&workspaceFolder=Notes%20Example%20API-ObjC&workspaceName=NotesExampleAPI&projectName=NotesExampleAPI&rootNamespace=NotesExampleAPI)


## Initialization

### 

Configuration variables can be set as following.
```Objc

```

# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [NotesController](#notes_controller)

## <a name="notes_controller"></a>![Class: ](https://apidocs.io/img/class.png ".NotesController") NotesController

### Get singleton instance
```objc
Notes* notes = [[Notes alloc]init] ;
```

### <a name="get_notes_async_with_q"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.getNotesAsyncWithQ") getNotesAsyncWithQ

> List all notes, optionally filtered by a query string


```objc
function getNotesAsyncWithQ:(NSString*) q
                completionBlock:(CompletedGetNotes) onCompleted(q)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| q |  ``` Optional ```  | An optional search query to filter the results |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* q = @"q";

    [self.notes getNotesAsyncWithQ: q  completionBlock:^(BOOL success, HttpContext* context, NSArray<NotesResponse> * response, NSError* error) { 
       //Add code here
    }];
```


### <a name="delete_notes_by_id_async_with_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.deleteNotesByIdAsyncWithId") deleteNotesByIdAsyncWithId

> Remove the specified note


```objc
function deleteNotesByIdAsyncWithId:(int) mid
                completionBlock:(CompletedDeleteNotesById) onCompleted(mid)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| mid |  ``` Required ```  | The `id` of the specific note |





#### Example Usage

```objc
    // Parameters for the API call
    int mid = [@"2" intValue];

    [self.notes deleteNotesByIdAsyncWithId: mid  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_notes_by_id_async_with_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.getNotesByIdAsyncWithId") getNotesByIdAsyncWithId

> Retrieve the specified note


```objc
function getNotesByIdAsyncWithId:(int) mid
                completionBlock:(CompletedGetNotesById) onCompleted(mid)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| mid |  ``` Required ```  | The `id` of the specific note |





#### Example Usage

```objc
    // Parameters for the API call
    int mid = [@"2" intValue];

    [self.notes getNotesByIdAsyncWithId: mid  completionBlock:^(BOOL success, HttpContext* context, NotesResponse* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="update_notes_by_id_async_with_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.updateNotesByIdAsyncWithId") updateNotesByIdAsyncWithId

> Update the specified note (allowing partial information)


```objc
function updateNotesByIdAsyncWithId:(int) mid
                body:(NSObject*) body
                completionBlock:(CompletedPatchNotesById) onCompleted(mid body : body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| mid |  ``` Required ```  | The `id` of the specific note |
| body |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    int mid = 171;
    NSObject* body = [[NSObject alloc]init];

    [self.notes updateNotesByIdAsyncWithId: mid body : body  completionBlock:^(BOOL success, HttpContext* context, NotesResponse* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_notes_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.createNotesAsyncWithBody") createNotesAsyncWithBody

> Create a new note in the collection


```objc
function createNotesAsyncWithBody:(NotesRequest*) body
                xTrackingExample:(enum XTrackingExampleEnum) xTrackingExample
                completionBlock:(CompletedPostNotes) onCompleted(body xTrackingExample : xTrackingExample)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| xTrackingExample |  ``` Optional ```  | You can specify request headers like this |





#### Example Usage

```objc
    // Parameters for the API call
    NotesRequest* body = (NotesRequest*) [APIHelper jsonDeserialize: @"{ \"title\": \"Return sweater\", \"dueInDays\": -2 }"
                toClass: NotesRequest.class];
    XTrackingExampleEnum xTrackingExample = (enum XTrackingExampleEnum) [XTrackingExampleEnumHelper xTrackingExampleEnumFromString: @"accounting"];

    [self.notes createNotesAsyncWithBody: body xTrackingExample : xTrackingExample  completionBlock:^(BOOL success, HttpContext* context, NotesResponse* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)



