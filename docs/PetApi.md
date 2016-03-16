# SwaggerPetstore.PetApi

All URIs are relative to *http://petstore.swagger.io/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addPet**](PetApi.md#addPet) | **POST** /pet | Add a new pet to the store
[**addPetUsingByteArray**](PetApi.md#addPetUsingByteArray) | **POST** /pet?testing_byte_array=true | Fake endpoint to test byte array in body parameter for adding a new pet to the store
[**deletePet**](PetApi.md#deletePet) | **DELETE** /pet/{petId} | Deletes a pet
[**findPetsByStatus**](PetApi.md#findPetsByStatus) | **GET** /pet/findByStatus | Finds Pets by status
[**findPetsByTags**](PetApi.md#findPetsByTags) | **GET** /pet/findByTags | Finds Pets by tags
[**getPetById**](PetApi.md#getPetById) | **GET** /pet/{petId} | Find pet by ID
[**getPetByIdInObject**](PetApi.md#getPetByIdInObject) | **GET** /pet/{petId}?response=inline_arbitrary_object | Fake endpoint to test inline arbitrary object return by &#39;Find pet by ID&#39;
[**petPetIdtestingByteArraytrueGet**](PetApi.md#petPetIdtestingByteArraytrueGet) | **GET** /pet/{petId}?testing_byte_array=true | Fake endpoint to test byte array return by &#39;Find pet by ID&#39;
[**updatePet**](PetApi.md#updatePet) | **PUT** /pet | Update an existing pet
[**updatePetWithForm**](PetApi.md#updatePetWithForm) | **POST** /pet/{petId} | Updates a pet in the store with form data
[**uploadFile**](PetApi.md#uploadFile) | **POST** /pet/{petId}/uploadImage | uploads an image


# **addPet** <a name="addPet"></a>
> addPet(opts)

Add a new pet to the store



### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');
var defaultClient = SwaggerPetstore.ApiClient.default;

// Configure OAuth2 access token for authorization: petstore_auth
var petstore_auth = defaultClient.authentications['petstore_auth'];
petstore_auth.accessToken = "YOUR ACCESS TOKEN"

var api = new SwaggerPetstore.PetApi()

var opts = { 
  'body': new SwaggerPetstore.Pet() // [Pet] Pet object that needs to be added to the store
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.addPet(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Pet**](Pet.md)| Pet object that needs to be added to the store | [optional] 

### Return type

nil (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: application/json, application/xml

# **addPetUsingByteArray** <a name="addPetUsingByteArray"></a>
> addPetUsingByteArray(opts)

Fake endpoint to test byte array in body parameter for adding a new pet to the store



### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');
var defaultClient = SwaggerPetstore.ApiClient.default;

// Configure OAuth2 access token for authorization: petstore_auth
var petstore_auth = defaultClient.authentications['petstore_auth'];
petstore_auth.accessToken = "YOUR ACCESS TOKEN"

var api = new SwaggerPetstore.PetApi()

var opts = { 
  'body': "B" // [String] Pet object in the form of byte array
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.addPetUsingByteArray(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **String**| Pet object in the form of byte array | [optional] 

### Return type

nil (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: application/json, application/xml

# **deletePet** <a name="deletePet"></a>
> deletePet(petId, opts)

Deletes a pet



### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');
var defaultClient = SwaggerPetstore.ApiClient.default;

// Configure OAuth2 access token for authorization: petstore_auth
var petstore_auth = defaultClient.authentications['petstore_auth'];
petstore_auth.accessToken = "YOUR ACCESS TOKEN"

var api = new SwaggerPetstore.PetApi()

var petId = 789; // [Integer] Pet id to delete

var opts = { 
  'apiKey': "apiKey_example" // [String] 
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.deletePet(petId, opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **Integer**| Pet id to delete | 
 **apiKey** | **String**|  | [optional] 

### Return type

nil (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

# **findPetsByStatus** <a name="findPetsByStatus"></a>
> [Pet] findPetsByStatus(opts)

Finds Pets by status

Multiple status values can be provided with comma separated strings

### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');
var defaultClient = SwaggerPetstore.ApiClient.default;

// Configure OAuth2 access token for authorization: petstore_auth
var petstore_auth = defaultClient.authentications['petstore_auth'];
petstore_auth.accessToken = "YOUR ACCESS TOKEN"

var api = new SwaggerPetstore.PetApi()

var opts = { 
  'status': ["available"] // [[String]] Status values that need to be considered for query
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.findPetsByStatus(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | [**[String]**](String.md)| Status values that need to be considered for query | [optional] [default to available]

### Return type

[**[Pet]**](Pet.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

# **findPetsByTags** <a name="findPetsByTags"></a>
> [Pet] findPetsByTags(opts)

Finds Pets by tags

Muliple tags can be provided with comma seperated strings. Use tag1, tag2, tag3 for testing.

### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');
var defaultClient = SwaggerPetstore.ApiClient.default;

// Configure OAuth2 access token for authorization: petstore_auth
var petstore_auth = defaultClient.authentications['petstore_auth'];
petstore_auth.accessToken = "YOUR ACCESS TOKEN"

var api = new SwaggerPetstore.PetApi()

var opts = { 
  'tags': ["tags_example"] // [[String]] Tags to filter by
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.findPetsByTags(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**[String]**](String.md)| Tags to filter by | [optional] 

### Return type

[**[Pet]**](Pet.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

# **getPetById** <a name="getPetById"></a>
> Pet getPetById(petId)

Find pet by ID

Returns a pet when ID &lt; 10.  ID &gt; 10 or nonintegers will simulate API error conditions

### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');
var defaultClient = SwaggerPetstore.ApiClient.default;

// Configure OAuth2 access token for authorization: petstore_auth
var petstore_auth = defaultClient.authentications['petstore_auth'];
petstore_auth.accessToken = "YOUR ACCESS TOKEN"

// Configure API key authorization: api_key
var api_key = defaultClient.authentications['api_key'];
api_key.apiKey = "YOUR API KEY"
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to nil)
//api_key.apiKeyPrefix['api_key'] = "Token"

var api = new SwaggerPetstore.PetApi()

var petId = 789; // [Integer] ID of pet that needs to be fetched


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.getPetById(petId, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **Integer**| ID of pet that needs to be fetched | 

### Return type

[**Pet**](Pet.md)

### Authorization

[petstore_auth](../README.md#petstore_auth), [api_key](../README.md#api_key)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

# **getPetByIdInObject** <a name="getPetByIdInObject"></a>
> InlineResponse200 getPetByIdInObject(petId)

Fake endpoint to test inline arbitrary object return by &#39;Find pet by ID&#39;

Returns a pet when ID &lt; 10.  ID &gt; 10 or nonintegers will simulate API error conditions

### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');
var defaultClient = SwaggerPetstore.ApiClient.default;

// Configure OAuth2 access token for authorization: petstore_auth
var petstore_auth = defaultClient.authentications['petstore_auth'];
petstore_auth.accessToken = "YOUR ACCESS TOKEN"

// Configure API key authorization: api_key
var api_key = defaultClient.authentications['api_key'];
api_key.apiKey = "YOUR API KEY"
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to nil)
//api_key.apiKeyPrefix['api_key'] = "Token"

var api = new SwaggerPetstore.PetApi()

var petId = 789; // [Integer] ID of pet that needs to be fetched


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.getPetByIdInObject(petId, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **Integer**| ID of pet that needs to be fetched | 

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[petstore_auth](../README.md#petstore_auth), [api_key](../README.md#api_key)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

# **petPetIdtestingByteArraytrueGet** <a name="petPetIdtestingByteArraytrueGet"></a>
> &#39;String&#39; petPetIdtestingByteArraytrueGet(petId)

Fake endpoint to test byte array return by &#39;Find pet by ID&#39;

Returns a pet when ID &lt; 10.  ID &gt; 10 or nonintegers will simulate API error conditions

### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');
var defaultClient = SwaggerPetstore.ApiClient.default;

// Configure OAuth2 access token for authorization: petstore_auth
var petstore_auth = defaultClient.authentications['petstore_auth'];
petstore_auth.accessToken = "YOUR ACCESS TOKEN"

// Configure API key authorization: api_key
var api_key = defaultClient.authentications['api_key'];
api_key.apiKey = "YOUR API KEY"
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to nil)
//api_key.apiKeyPrefix['api_key'] = "Token"

var api = new SwaggerPetstore.PetApi()

var petId = 789; // [Integer] ID of pet that needs to be fetched


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.petPetIdtestingByteArraytrueGet(petId, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **Integer**| ID of pet that needs to be fetched | 

### Return type

**&#39;String&#39;**

### Authorization

[petstore_auth](../README.md#petstore_auth), [api_key](../README.md#api_key)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

# **updatePet** <a name="updatePet"></a>
> updatePet(opts)

Update an existing pet



### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');
var defaultClient = SwaggerPetstore.ApiClient.default;

// Configure OAuth2 access token for authorization: petstore_auth
var petstore_auth = defaultClient.authentications['petstore_auth'];
petstore_auth.accessToken = "YOUR ACCESS TOKEN"

var api = new SwaggerPetstore.PetApi()

var opts = { 
  'body': new SwaggerPetstore.Pet() // [Pet] Pet object that needs to be added to the store
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.updatePet(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Pet**](Pet.md)| Pet object that needs to be added to the store | [optional] 

### Return type

nil (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: application/json, application/xml

# **updatePetWithForm** <a name="updatePetWithForm"></a>
> updatePetWithForm(petId, opts)

Updates a pet in the store with form data



### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');
var defaultClient = SwaggerPetstore.ApiClient.default;

// Configure OAuth2 access token for authorization: petstore_auth
var petstore_auth = defaultClient.authentications['petstore_auth'];
petstore_auth.accessToken = "YOUR ACCESS TOKEN"

var api = new SwaggerPetstore.PetApi()

var petId = "petId_example"; // [String] ID of pet that needs to be updated

var opts = { 
  'name': "name_example", // [String] Updated name of the pet
  'status': "status_example" // [String] Updated status of the pet
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.updatePetWithForm(petId, opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **String**| ID of pet that needs to be updated | 
 **name** | **String**| Updated name of the pet | [optional] 
 **status** | **String**| Updated status of the pet | [optional] 

### Return type

nil (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

# **uploadFile** <a name="uploadFile"></a>
> uploadFile(petId, opts)

uploads an image



### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');
var defaultClient = SwaggerPetstore.ApiClient.default;

// Configure OAuth2 access token for authorization: petstore_auth
var petstore_auth = defaultClient.authentications['petstore_auth'];
petstore_auth.accessToken = "YOUR ACCESS TOKEN"

var api = new SwaggerPetstore.PetApi()

var petId = 789; // [Integer] ID of pet to update

var opts = { 
  'additionalMetadata': "additionalMetadata_example", // [String] Additional data to pass to server
  'file': "/path/to/file.txt" // [File] file to upload
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.uploadFile(petId, opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **Integer**| ID of pet to update | 
 **additionalMetadata** | **String**| Additional data to pass to server | [optional] 
 **file** | **File**| file to upload | [optional] 

### Return type

nil (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, application/xml

