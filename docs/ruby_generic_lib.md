# Getting started

This is an example of a simple API for a "notes" service

## How to Build

This client library is a Ruby gem which can be compiled and used in your Ruby and Ruby on Rails project. This library requires a few gems from the RubyGems repository.

1. Open the command line interface or the terminal and navigate to the folder containing the source code.
2. Run ``` gem build notes_example_api.gemspec ``` to build the gem.
3. Once built, the gem can be installed on the current work environment using ``` gem install notes_example_api-1.0.0.gem ```

![Building Gem](https://apidocs.io/illustration/ruby?step=buildSDK&workspaceFolder=Notes%20Example%20API-Ruby&workspaceName=Notes%20Example%20API-Ruby&projectName=notes_example_api&gemName=notes_example_api&gemVer=1.0.0)

## How to Use

The following section explains how to use the NotesExampleApi Ruby Gem in a new Rails project using RubyMine&trade;. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

### 1. Starting a new project

Close any existing projects in RubyMine&trade; by selecting ``` File -> Close Project ```. Next, click on ``` Create New Project ``` to create a new project from scratch.

![Create a new project in RubyMine](https://apidocs.io/illustration/ruby?step=createNewProject0&workspaceFolder=Notes%20Example%20API-Ruby&workspaceName=NotesExampleApi&projectName=notes_example_api&gemName=notes_example_api&gemVer=1.0.0)

Next, provide ``` TestApp ``` as the project name, choose ``` Rails Application ``` as the project type, and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 1](https://apidocs.io/illustration/ruby?step=createNewProject1&workspaceFolder=Notes%20Example%20API-Ruby&workspaceName=NotesExampleApi&projectName=notes_example_api&gemName=notes_example_api&gemVer=1.0.0)

In the next dialog make sure that correct *Ruby SDK* is being used (minimum 2.0.0) and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 2](https://apidocs.io/illustration/ruby?step=createNewProject2&workspaceFolder=Notes%20Example%20API-Ruby&workspaceName=NotesExampleApi&projectName=notes_example_api&gemName=notes_example_api&gemVer=1.0.0)

This will create a new Rails Application project with an existing set of files and folder.

### 2. Add reference of the gem

In order to use the NotesExampleApi gem in the new project we must add a gem reference. Locate the ```Gemfile``` in the *Project Explorer* window under the ``` TestApp ``` project node. The file contains references to all gems being used in the project. Here, add the reference to the library gem by adding the following line: ``` gem 'notes_example_api', '~> 1.0.0' ```

![Add references of the Gemfile](https://apidocs.io/illustration/ruby?step=addReference&workspaceFolder=Notes%20Example%20API-Ruby&workspaceName=NotesExampleApi&projectName=notes_example_api&gemName=notes_example_api&gemVer=1.0.0)

### 3. Adding a new Rails Controller

Once the ``` TestApp ``` project is created, a folder named ``` controllers ``` will be visible in the *Project Explorer* under the following path: ``` TestApp > app > controllers ```. Right click on this folder and select ``` New -> Run Rails Generator... ```.

![Run Rails Generator on Controllers Folder](https://apidocs.io/illustration/ruby?step=addCode0&workspaceFolder=Notes%20Example%20API-Ruby&workspaceName=NotesExampleApi&projectName=notes_example_api&gemName=notes_example_api&gemVer=1.0.0)

Selecting the said option will popup a small window where the generator names are displayed. Here, select the ``` controller ``` template.

![Create a new Controller](https://apidocs.io/illustration/ruby?step=addCode1&workspaceFolder=Notes%20Example%20API-Ruby&workspaceName=NotesExampleApi&projectName=notes_example_api&gemName=notes_example_api&gemVer=1.0.0)

Next, a popup window will ask you for a Controller name and included Actions. For controller name provide ``` Hello ``` and include an action named ``` Index ``` and click ``` OK ```.

![Add a new Controller](https://apidocs.io/illustration/ruby?step=addCode2&workspaceFolder=Notes%20Example%20API-Ruby&workspaceName=NotesExampleApi&projectName=notes_example_api&gemName=notes_example_api&gemVer=1.0.0)

A new controller class anmed ``` HelloController ``` will be created in a file named ``` hello_controller.rb ``` containing a method named ``` Index ```. In this method, add code for initialization and a sample for its usage.

![Initialize the library](https://apidocs.io/illustration/ruby?step=addCode3&workspaceFolder=Notes%20Example%20API-Ruby&workspaceName=NotesExampleApi&projectName=notes_example_api&gemName=notes_example_api&gemVer=1.0.0)

## How to Test

You can test the generated SDK and the server with automatically generated test
cases as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke: `bundle exec rake`

## Initialization

### 

API client can be initialized as following.

```ruby

client = NotesExampleApi::NotesExampleApiClient.new
```

The added initlization code can be debugged by putting a breakpoint in the ``` Index ``` method and running the project in debug mode by selecting ``` Run -> Debug 'Development: TestApp' ```.

![Debug the TestApp](https://apidocs.io/illustration/ruby?step=addCode4&workspaceFolder=Notes%20Example%20API-Ruby&workspaceName=NotesExampleApi&projectName=notes_example_api&gemName=notes_example_api&gemVer=1.0.0&initLine=client%2520%253D%2520NotesExampleApiClient.new)



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [NotesController](#notes_controller)

## <a name="notes_controller"></a>![Class: ](https://apidocs.io/img/class.png ".NotesController") NotesController

### Get singleton instance

The singleton instance of the ``` NotesController ``` class can be accessed from the API Client.

```ruby
notes = client.notes
```

### <a name="get_notes"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.get_notes") get_notes

> List all notes, optionally filtered by a query string


```ruby
def get_notes(q = nil); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| q |  ``` Optional ```  | An optional search query to filter the results |


#### Example Usage

```ruby
q = 'q'

result = notes.get_notes(q)

```


### <a name="delete_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.delete_notes_by_id") delete_notes_by_id

> Remove the specified note


```ruby
def delete_notes_by_id(id); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |


#### Example Usage

```ruby
id = 2

notes.delete_notes_by_id(id)

```


### <a name="get_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.get_notes_by_id") get_notes_by_id

> Retrieve the specified note


```ruby
def get_notes_by_id(id); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |


#### Example Usage

```ruby
id = 2

result = notes.get_notes_by_id(id)

```


### <a name="update_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.update_notes_by_id") update_notes_by_id

> Update the specified note (allowing partial information)


```ruby
def update_notes_by_id(id,
                           body); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
id = 212
body = Object.new

result = notes.update_notes_by_id(id, body)

```


### <a name="create_notes"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.create_notes") create_notes

> Create a new note in the collection


```ruby
def create_notes(body,
                     x_tracking_example = nil); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| x_tracking_example |  ``` Optional ```  | You can specify request headers like this |


#### Example Usage

```ruby
body_value = "{ \"title\": \"Return sweater\", \"dueInDays\": -2 }";
body = JSON.parse(body_value);
x_tracking_example = NotesExampleApi::XTrackingExampleEnum::ACCOUNTING

result = notes.create_notes(body, x_tracking_example)

```


[Back to List of Controllers](#list_of_controllers)



