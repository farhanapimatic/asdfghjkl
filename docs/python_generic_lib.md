# Getting started

This is an example of a simple API for a "notes" service

## How to Build


You must have Python 2 >=2.7.9 or Python 3 >=3.4 installed on your system to install and run this SDK. This SDK package depends on other Python packages like nose, jsonpickle etc. 
These dependencies are defined in the ```requirements.txt``` file that comes with the SDK.
To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type ```pip --version```.
This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including ```requirements.txt```) for the SDK.
* Run the command ```pip install -r requirements.txt```. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?step=installDependencies&workspaceFolder=Notes%20Example%20API-Python)


## How to Use

The following section explains how to use the Notesexampleapi SDK package in a new project.

### 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=pyCharm)

Click on ```Open``` in PyCharm to browse to your generated SDK directory and then click ```OK```.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=openProject0&workspaceFolder=Notes%20Example%20API-Python)     

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=openProject1&workspaceFolder=Notes%20Example%20API-Python&projectName=notesexampleapi)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=createDirectory&workspaceFolder=Notes%20Example%20API-Python&projectName=notesexampleapi)

Name the directory as "test"

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=nameDirectory)
   
Add a python file to this project with the name "testsdk"

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=createFile&workspaceFolder=Notes%20Example%20API-Python&projectName=notesexampleapi)

Name it "testsdk"

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```Python
from notesexampleapi.notesexampleapi_client import NotesexampleapiClient
```

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=projectFiles&workspaceFolder=Notes%20Example%20API-Python&libraryName=notesexampleapi.notesexampleapi_client&projectName=notesexampleapi)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

### 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on ```Run```

![Run Test Project - Step 1](https://apidocs.io/illustration/python?step=runProject&workspaceFolder=Notes%20Example%20API-Python&libraryName=notesexampleapi.notesexampleapi_client&projectName=notesexampleapi)


## How to Test

You can test the generated SDK and the server with automatically generated test
cases. unittest is used as the testing framework and nose is used as the test
runner. You can run the tests as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke 'pip install -r test-requirements.txt'
  3. Invoke 'nosetests'

## Initialization

### 

API client can be initialized as following.

```python

client = NotesexampleapiClient()
```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [NotesController](#notes_controller)

## <a name="notes_controller"></a>![Class: ](https://apidocs.io/img/class.png ".NotesController") NotesController

### Get controller instance

An instance of the ``` NotesController ``` class can be accessed from the API Client.

```python
 notes_client = client.notes
```

### <a name="get_notes"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.get_notes") get_notes

> List all notes, optionally filtered by a query string

```python
def get_notes(self,
                  q=None)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| q |  ``` Optional ```  | An optional search query to filter the results |



#### Example Usage

```python
q = 'q'

result = notes_client.get_notes(q)

```


### <a name="delete_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.delete_notes_by_id") delete_notes_by_id

> Remove the specified note

```python
def delete_notes_by_id(self,
                           id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |



#### Example Usage

```python
id = 2

notes_client.delete_notes_by_id(id)

```


### <a name="get_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.get_notes_by_id") get_notes_by_id

> Retrieve the specified note

```python
def get_notes_by_id(self,
                        id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |



#### Example Usage

```python
id = 2

result = notes_client.get_notes_by_id(id)

```


### <a name="update_notes_by_id"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.update_notes_by_id") update_notes_by_id

> Update the specified note (allowing partial information)

```python
def update_notes_by_id(self,
                           id,
                           body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| id |  ``` Required ```  | The `id` of the specific note |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
id = 212
body = object()

result = notes_client.update_notes_by_id(id, body)

```


### <a name="create_notes"></a>![Method: ](https://apidocs.io/img/method.png ".NotesController.create_notes") create_notes

> Create a new note in the collection

```python
def create_notes(self,
                     body,
                     x_tracking_example=None)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| xTrackingExample |  ``` Optional ```  | You can specify request headers like this |



#### Example Usage

```python
body_value = "{ \"title\": \"Return sweater\", \"dueInDays\": -2 }"
body = json.loads(body_value)
x_tracking_example = XTrackingExampleEnum.ACCOUNTING

result = notes_client.create_notes(body, x_tracking_example)

```


[Back to List of Controllers](#list_of_controllers)



