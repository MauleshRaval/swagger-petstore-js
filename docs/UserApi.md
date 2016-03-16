# SwaggerPetstore.UserApi

All URIs are relative to *http://petstore.swagger.io/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createUser**](UserApi.md#createUser) | **POST** /user | Create user
[**createUsersWithArrayInput**](UserApi.md#createUsersWithArrayInput) | **POST** /user/createWithArray | Creates list of users with given input array
[**createUsersWithListInput**](UserApi.md#createUsersWithListInput) | **POST** /user/createWithList | Creates list of users with given input array
[**deleteUser**](UserApi.md#deleteUser) | **DELETE** /user/{username} | Delete user
[**getUserByName**](UserApi.md#getUserByName) | **GET** /user/{username} | Get user by user name
[**loginUser**](UserApi.md#loginUser) | **GET** /user/login | Logs user into the system
[**logoutUser**](UserApi.md#logoutUser) | **GET** /user/logout | Logs out current logged in user session
[**updateUser**](UserApi.md#updateUser) | **PUT** /user/{username} | Updated user


# **createUser**
> createUser(opts)

Create user

This can only be done by the logged in user.

### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');

var api = new SwaggerPetstore.UserApi()

var opts = { 
  'body': new SwaggerPetstore.User() // [User] Created user object
};
<#usePromises>
api.createUser(opts).then(function() {
  console.log('API called successfully.');
}, function(error) {
  console.error(error);
});

</usePromises><^usePromises>
var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.createUser(opts<#hasParams>, </hasParams>callback);
</usePromises>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**User**](User.md)| Created user object | [optional] 

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

# **createUsersWithArrayInput**
> createUsersWithArrayInput(opts)

Creates list of users with given input array



### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');

var api = new SwaggerPetstore.UserApi()

var opts = { 
  'body': [new SwaggerPetstore.User()] // [[User]] List of user object
};
<#usePromises>
api.createUsersWithArrayInput(opts).then(function() {
  console.log('API called successfully.');
}, function(error) {
  console.error(error);
});

</usePromises><^usePromises>
var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.createUsersWithArrayInput(opts<#hasParams>, </hasParams>callback);
</usePromises>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**[User]**](User.md)| List of user object | [optional] 

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

# **createUsersWithListInput**
> createUsersWithListInput(opts)

Creates list of users with given input array



### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');

var api = new SwaggerPetstore.UserApi()

var opts = { 
  'body': [new SwaggerPetstore.User()] // [[User]] List of user object
};
<#usePromises>
api.createUsersWithListInput(opts).then(function() {
  console.log('API called successfully.');
}, function(error) {
  console.error(error);
});

</usePromises><^usePromises>
var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.createUsersWithListInput(opts<#hasParams>, </hasParams>callback);
</usePromises>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**[User]**](User.md)| List of user object | [optional] 

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

# **deleteUser**
> deleteUser(username)

Delete user

This can only be done by the logged in user.

### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');
var defaultClient = SwaggerPetstore.ApiClient.default;

// Configure HTTP basic authorization: test_http_basic
var test_http_basic = defaultClient.authentications['test_http_basic'];
test_http_basic.username = 'YOUR USERNAME'
test_http_basic.password = 'YOUR PASSWORD'
end

var api = new SwaggerPetstore.UserApi()

<#usePromises>
api.deleteUser(username).then(function() {
  console.log('API called successfully.');
}, function(error) {
  console.error(error);
});

</usePromises><^usePromises>
var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.deleteUser(username<#hasParams>, </hasParams>callback);
</usePromises>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **String**| The name that needs to be deleted | 

### Return type

nil (empty response body)

### Authorization

[test_http_basic](../README.md#test_http_basic)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

# **getUserByName**
> User getUserByName(username)

Get user by user name



### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');

var api = new SwaggerPetstore.UserApi()

<#usePromises>
api.getUserByName(username).then(function(data) {
  console.log('API called successfully. Returned data: ' + data);
}, function(error) {
  console.error(error);
});

</usePromises><^usePromises>
var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.getUserByName(username<#hasParams>, </hasParams>callback);
</usePromises>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **String**| The name that needs to be fetched. Use user1 for testing. | 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

# **loginUser**
> &#39;String&#39; loginUser(opts)

Logs user into the system



### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');

var api = new SwaggerPetstore.UserApi()

var opts = { 
  'username': "username_example" // [String] The user name for login
  'password': "password_example" // [String] The password for login in clear text
};
<#usePromises>
api.loginUser(opts).then(function(data) {
  console.log('API called successfully. Returned data: ' + data);
}, function(error) {
  console.error(error);
});

</usePromises><^usePromises>
var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.loginUser(opts<#hasParams>, </hasParams>callback);
</usePromises>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **String**| The user name for login | [optional] 
 **password** | **String**| The password for login in clear text | [optional] 

### Return type

**&#39;String&#39;**

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

# **logoutUser**
> logoutUser

Logs out current logged in user session



### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');

var api = new SwaggerPetstore.UserApi()
<#usePromises>
api.logoutUser().then(function() {
  console.log('API called successfully.');
}, function(error) {
  console.error(error);
});

</usePromises><^usePromises>
var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.logoutUser(<#hasParams>, </hasParams>callback);
</usePromises>
```

### Parameters
This endpoint does not need any parameter.

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

# **updateUser**
> updateUser(usernameopts)

Updated user

This can only be done by the logged in user.

### Example
```javascript
var SwaggerPetstore = require('swagger-petstore');

var api = new SwaggerPetstore.UserApi()

var opts = { 
  'body': new SwaggerPetstore.User() // [User] Updated user object
};
<#usePromises>
api.updateUser(usernameopts).then(function() {
  console.log('API called successfully.');
}, function(error) {
  console.error(error);
});

</usePromises><^usePromises>
var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.updateUser(usernameopts<#hasParams>, </hasParams>callback);
</usePromises>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **String**| name that need to be deleted | 
 **body** | [**User**](User.md)| Updated user object | [optional] 

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

