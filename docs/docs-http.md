# 

**`API Version:`** `v2`

This is an example of a simple API for a "notes" service



## Base URL

The base URL for this API is `http://example.com/api`









# <a name="api_reference"></a>API Reference

* [notes](#notes)

## <a name="notes"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "notes") notes


### <a name="notes"></a>![Endpoint: ](https://apidocs.io/img/method.png "Notes") Notes


**`GET`** `/notes`

> List all notes, optionally filtered by a query string




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| q | string |  ``` Optional ```  | An optional search query to filter the results | `shopping` | 

#### Responses
**200** 


 *Example Body* (**[[Notes response](#notes_response)]**) 

```
[
  {
    "id": 2,
    "title": "Return sweater",
    "status": "overdue",
    "dueInDays": -2
  }
]
```


### <a name="notes_by_id"></a>![Endpoint: ](https://apidocs.io/img/method.png "NotesById") NotesById


**`DELETE`** `/notes/{id}`

> Remove the specified note




#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ----------------------------------- |
| id | number |  ``` Required ```  | The `id` of the specific note | `2` | 

#### Responses
**200**


### <a name="notes_by_id"></a>![Endpoint: ](https://apidocs.io/img/method.png "NotesById") NotesById


**`GET`** `/notes/{id}`

> Retrieve the specified note




#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ----------------------------------- |
| id | number |  ``` Required ```  | The `id` of the specific note | `2` | 

#### Responses
**200** 


 *Example Body* (**[Notes response](#notes_response)**) 

```
{
  "id": 2,
  "title": "Return sweater",
  "status": "overdue",
  "dueInDays": -2
}
```


### <a name="notes_by_id"></a>![Endpoint: ](https://apidocs.io/img/method.png "NotesById") NotesById


**`PATCH`** `/notes/{id}`

> Update the specified note (allowing partial information)




#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ----------------------------------- |
| id | number |  ``` Required ```  | The `id` of the specific note | `2` | 

#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| object |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{}
``` 

#### Responses
**200** 


 *Example Body* (**[Notes response](#notes_response)**) 

```
{
  "id": 2,
  "title": "Return sweater",
  "status": "overdue",
  "dueInDays": -2
}
```


### <a name="notes"></a>![Endpoint: ](https://apidocs.io/img/method.png "Notes") Notes


**`POST`** `/notes`

> Create a new note in the collection




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;
>X-Tracking-Example=accounting;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [Notes request](#notes_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "title": "Return sweater",
  "dueInDays": -2
}
``` 

#### Responses
**200** 


 *Example Body* (**[Notes response](#notes_response)**) 

```
{
  "id": 2,
  "title": "Return sweater",
  "status": "overdue",
  "dueInDays": -2
}
```


[Back to API Reference](#api_reference)

# <a name="models"></a> Models

### List of Models

* [Notes request](#notes_request)
* [X-Tracking-ExampleEnum](#x_tracking_example_enum)
* [Notes response](#notes_response)
* [Object](#object)
## <a name="notes_request"></a>![Type: ](https://apidocs.io/img/method.png "Notes request") Notes request



> TODO: Add a method description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| title | string |  ``` Required ```  | TODO: Add a property description | 
| dueInDays | number |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "title": "Return sweater",
  "dueInDays": -2
}
```



## <a name="x_tracking_example_enum"></a>![Type: ](https://apidocs.io/img/method.png "X-Tracking-ExampleEnum") X-Tracking-ExampleEnum



> TODO: Add a method description





This type must take a value from the following `string` enumeration of values:

| Name | Value | Description |
| ---- | ----- | ----------- |
| accounting | `accounting` | TODO: Add description | 
| payroll | `payroll` | TODO: Add description | 
| finance | `finance` | TODO: Add description | 



#### Example
```
accounting
```



## <a name="notes_response"></a>![Type: ](https://apidocs.io/img/method.png "Notes response") Notes response



> TODO: Add a method description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| id | number |  ``` Required ```  | TODO: Add a property description | 
| title | string |  ``` Required ```  | TODO: Add a property description | 
| status | string |  ``` Required ```  | TODO: Add a property description | 
| dueInDays | number |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "id": 2,
  "title": "Return sweater",
  "status": "overdue",
  "dueInDays": -2
}
```



## <a name="object"></a>![Type: ](https://apidocs.io/img/method.png "Object") Object



> TODO: Add a method description





#### Example
```
{}
```




