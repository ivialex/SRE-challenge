# swagger_client.DefaultApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**attach_instance**](DefaultApi.md#attach_instance) | **POST** /elb/{elbName} | 
[**elb_elb_name_delete**](DefaultApi.md#elb_elb_name_delete) | **DELETE** /elb/{elbName} | 
[**healthcheck_get**](DefaultApi.md#healthcheck_get) | **GET** /healthcheck | 
[**list_machines_elb**](DefaultApi.md#list_machines_elb) | **GET** /elb/{elbName} | 


# **attach_instance**
> MachineInfo attach_instance(elb_name, machine_id=machine_id)



Attach an instance on the load balancer

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure HTTP basic authorization: basicAuth
configuration = swagger_client.Configuration()
configuration.username = 'YOUR_USERNAME'
configuration.password = 'YOUR_PASSWORD'

# create an instance of the API class
api_instance = swagger_client.DefaultApi(swagger_client.ApiClient(configuration))
elb_name = 'elb_name_example' # str | pass the load balancer name
machine_id = swagger_client.MachineId() # MachineId | instance identifier (optional)

try:
    api_response = api_instance.attach_instance(elb_name, machine_id=machine_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DefaultApi->attach_instance: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **elb_name** | **str**| pass the load balancer name | 
 **machine_id** | [**MachineId**](MachineId.md)| instance identifier | [optional] 

### Return type

[**MachineInfo**](MachineInfo.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **elb_elb_name_delete**
> MachineInfo elb_elb_name_delete(elb_name, machine_id=machine_id)



Detach an instance from the load balancer

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure HTTP basic authorization: basicAuth
configuration = swagger_client.Configuration()
configuration.username = 'YOUR_USERNAME'
configuration.password = 'YOUR_PASSWORD'

# create an instance of the API class
api_instance = swagger_client.DefaultApi(swagger_client.ApiClient(configuration))
elb_name = 'elb_name_example' # str | pass the load balancer name
machine_id = swagger_client.MachineId() # MachineId | instance identifier (optional)

try:
    api_response = api_instance.elb_elb_name_delete(elb_name, machine_id=machine_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DefaultApi->elb_elb_name_delete: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **elb_name** | **str**| pass the load balancer name | 
 **machine_id** | [**MachineId**](MachineId.md)| instance identifier | [optional] 

### Return type

[**MachineInfo**](MachineInfo.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **healthcheck_get**
> healthcheck_get()



API health check

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure HTTP basic authorization: basicAuth
configuration = swagger_client.Configuration()
configuration.username = 'YOUR_USERNAME'
configuration.password = 'YOUR_PASSWORD'

# create an instance of the API class
api_instance = swagger_client.DefaultApi(swagger_client.ApiClient(configuration))

try:
    api_instance.healthcheck_get()
except ApiException as e:
    print("Exception when calling DefaultApi->healthcheck_get: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_machines_elb**
> list[MachineInfo] list_machines_elb(elb_name)



List machines attached to a particular load balancer

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure HTTP basic authorization: basicAuth
configuration = swagger_client.Configuration()
configuration.username = 'YOUR_USERNAME'
configuration.password = 'YOUR_PASSWORD'

# create an instance of the API class
api_instance = swagger_client.DefaultApi(swagger_client.ApiClient(configuration))
elb_name = 'elb_name_example' # str | pass the load balancer name

try:
    api_response = api_instance.list_machines_elb(elb_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DefaultApi->list_machines_elb: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **elb_name** | **str**| pass the load balancer name | 

### Return type

[**list[MachineInfo]**](MachineInfo.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

