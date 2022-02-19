--------

--------

# AssociatePersonasToEntities<a name="API_AssociatePersonasToEntities"></a>

Defines the specific permissions of users or groups in your AWS SSO identity source with access to your Amazon Kendra experience\. You can create an Amazon Kendra experience such as a search application\. For more information on creating a search application experience, see [Building a search experience with no code](https://docs.aws.amazon.com/kendra/latest/dg/deploying-search-experience-no-code.html)\.

## Request Syntax<a name="API_AssociatePersonasToEntities_RequestSyntax"></a>

```
{
   "Id": "string",
   "IndexId": "string",
   "Personas": [ 
      { 
         "EntityId": "string",
         "Persona": "string"
      }
   ]
}
```

## Request Parameters<a name="API_AssociatePersonasToEntities_RequestParameters"></a>

For information about the parameters that are common to all actions, see [Common Parameters](CommonParameters.md)\.

The request accepts the following data in JSON format\.

 ** [ Id ](#API_AssociatePersonasToEntities_RequestSyntax) **   <a name="Kendra-AssociatePersonasToEntities-request-Id"></a>
The identifier of your Amazon Kendra experience\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 36\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9_-]*`   
Required: Yes

 ** [ IndexId ](#API_AssociatePersonasToEntities_RequestSyntax) **   <a name="Kendra-AssociatePersonasToEntities-request-IndexId"></a>
The identifier of the index for your Amazon Kendra experience\.  
Type: String  
Length Constraints: Fixed length of 36\.  
Pattern: `[a-zA-Z0-9][a-zA-Z0-9-]*`   
Required: Yes

 ** [ Personas ](#API_AssociatePersonasToEntities_RequestSyntax) **   <a name="Kendra-AssociatePersonasToEntities-request-Personas"></a>
The personas that define the specific permissions of users or groups in your AWS SSO identity source\. The available personas or access roles are `Owner` and `Viewer`\. For more information on these personas, see [Providing access to your search page](https://docs.aws.amazon.com/kendra/latest/dg/deploying-search-experience-no-code.html#access-search-experience)\.  
Type: Array of [ EntityPersonaConfiguration ](API_EntityPersonaConfiguration.md) objects  
Array Members: Minimum number of 1 item\. Maximum number of 25 items\.  
Required: Yes

## Response Syntax<a name="API_AssociatePersonasToEntities_ResponseSyntax"></a>

```
{
   "FailedEntityList": [ 
      { 
         "EntityId": "string",
         "ErrorMessage": "string"
      }
   ]
}
```

## Response Elements<a name="API_AssociatePersonasToEntities_ResponseElements"></a>

If the action is successful, the service sends back an HTTP 200 response\.

The following data is returned in JSON format by the service\.

 ** [ FailedEntityList ](#API_AssociatePersonasToEntities_ResponseSyntax) **   <a name="Kendra-AssociatePersonasToEntities-response-FailedEntityList"></a>
Lists the users or groups in your AWS SSO identity source that failed to properly configure with your Amazon Kendra experience\.  
Type: Array of [ FailedEntity ](API_FailedEntity.md) objects  
Array Members: Minimum number of 1 item\. Maximum number of 25 items\.

## Errors<a name="API_AssociatePersonasToEntities_Errors"></a>

For information about the errors that are common to all actions, see [Common Errors](CommonErrors.md)\.

 ** AccessDeniedException **   
  
HTTP Status Code: 400

 ** InternalServerException **   
  
HTTP Status Code: 500

 ** ResourceAlreadyExistException **   
  
HTTP Status Code: 400

 ** ResourceNotFoundException **   
  
HTTP Status Code: 400

 ** ThrottlingException **   
  
HTTP Status Code: 400

 ** ValidationException **   
  
HTTP Status Code: 400

## See Also<a name="API_AssociatePersonasToEntities_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:
+  [ AWS Command Line Interface](https://docs.aws.amazon.com/goto/aws-cli/kendra-2019-02-03/AssociatePersonasToEntities) 
+  [ AWS SDK for \.NET](https://docs.aws.amazon.com/goto/DotNetSDKV3/kendra-2019-02-03/AssociatePersonasToEntities) 
+  [ AWS SDK for C\+\+](https://docs.aws.amazon.com/goto/SdkForCpp/kendra-2019-02-03/AssociatePersonasToEntities) 
+  [ AWS SDK for Go](https://docs.aws.amazon.com/goto/SdkForGoV1/kendra-2019-02-03/AssociatePersonasToEntities) 
+  [ AWS SDK for Java V2](https://docs.aws.amazon.com/goto/SdkForJavaV2/kendra-2019-02-03/AssociatePersonasToEntities) 
+  [ AWS SDK for JavaScript](https://docs.aws.amazon.com/goto/AWSJavaScriptSDK/kendra-2019-02-03/AssociatePersonasToEntities) 
+  [ AWS SDK for PHP V3](https://docs.aws.amazon.com/goto/SdkForPHPV3/kendra-2019-02-03/AssociatePersonasToEntities) 
+  [ AWS SDK for Python](https://docs.aws.amazon.com/goto/boto3/kendra-2019-02-03/AssociatePersonasToEntities) 
+  [ AWS SDK for Ruby V3](https://docs.aws.amazon.com/goto/SdkForRubyV3/kendra-2019-02-03/AssociatePersonasToEntities) 