# ory/keto-client

A cloud native access control server providing best-practice patterns (RBAC, ABAC, ACL, AWS IAM Policies, Kubernetes Roles, ...) via REST APIs.

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: v0.0.0-alpha.33
- Build package: org.openapitools.codegen.languages.PhpClientCodegen
For more information, please visit [https://www.ory.sh](https://www.ory.sh)

## Requirements

PHP 5.5 and later

## Installation & Usage

### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/ory/keto-client-php.git"
    }
  ],
  "require": {
    "ory/keto-client-php": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/ory/keto-client/vendor/autoload.php');
```

## Tests

To run the unit tests:

```bash
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Ory\Keto\Client\Api\EnginesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$flavor = 'flavor_example'; // string | The ORY Access Control Policy flavor. Can be \"regex\", \"glob\", and \"exact\".
$id = 'id_example'; // string | The ID of the ORY Access Control Policy Role.
$body = new \Ory\Keto\Client\Model\AddOryAccessControlPolicyRoleMembersBody(); // \Ory\Keto\Client\Model\AddOryAccessControlPolicyRoleMembersBody | 

try {
    $result = $apiInstance->addOryAccessControlPolicyRoleMembers($flavor, $id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnginesApi->addOryAccessControlPolicyRoleMembers: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*EnginesApi* | [**addOryAccessControlPolicyRoleMembers**](docs/Api/EnginesApi.md#addoryaccesscontrolpolicyrolemembers) | **PUT** /engines/acp/ory/{flavor}/roles/{id}/members | Add a member to an ORY Access Control Policy Role
*EnginesApi* | [**deleteOryAccessControlPolicy**](docs/Api/EnginesApi.md#deleteoryaccesscontrolpolicy) | **DELETE** /engines/acp/ory/{flavor}/policies/{id} | 
*EnginesApi* | [**deleteOryAccessControlPolicyRole**](docs/Api/EnginesApi.md#deleteoryaccesscontrolpolicyrole) | **DELETE** /engines/acp/ory/{flavor}/roles/{id} | Delete an ORY Access Control Policy Role
*EnginesApi* | [**doOryAccessControlPoliciesAllow**](docs/Api/EnginesApi.md#dooryaccesscontrolpoliciesallow) | **POST** /engines/acp/ory/{flavor}/allowed | Check if a request is allowed
*EnginesApi* | [**getOryAccessControlPolicy**](docs/Api/EnginesApi.md#getoryaccesscontrolpolicy) | **GET** /engines/acp/ory/{flavor}/policies/{id} | 
*EnginesApi* | [**getOryAccessControlPolicyRole**](docs/Api/EnginesApi.md#getoryaccesscontrolpolicyrole) | **GET** /engines/acp/ory/{flavor}/roles/{id} | Get an ORY Access Control Policy Role
*EnginesApi* | [**listOryAccessControlPolicies**](docs/Api/EnginesApi.md#listoryaccesscontrolpolicies) | **GET** /engines/acp/ory/{flavor}/policies | 
*EnginesApi* | [**listOryAccessControlPolicyRoles**](docs/Api/EnginesApi.md#listoryaccesscontrolpolicyroles) | **GET** /engines/acp/ory/{flavor}/roles | List ORY Access Control Policy Roles
*EnginesApi* | [**removeOryAccessControlPolicyRoleMembers**](docs/Api/EnginesApi.md#removeoryaccesscontrolpolicyrolemembers) | **DELETE** /engines/acp/ory/{flavor}/roles/{id}/members/{member} | Remove a member from an ORY Access Control Policy Role
*EnginesApi* | [**upsertOryAccessControlPolicy**](docs/Api/EnginesApi.md#upsertoryaccesscontrolpolicy) | **PUT** /engines/acp/ory/{flavor}/policies | 
*EnginesApi* | [**upsertOryAccessControlPolicyRole**](docs/Api/EnginesApi.md#upsertoryaccesscontrolpolicyrole) | **PUT** /engines/acp/ory/{flavor}/roles | Upsert an ORY Access Control Policy Role
*HealthApi* | [**isInstanceAlive**](docs/Api/HealthApi.md#isinstancealive) | **GET** /health/alive | Check alive status
*HealthApi* | [**isInstanceReady**](docs/Api/HealthApi.md#isinstanceready) | **GET** /health/ready | Check readiness status
*VersionApi* | [**getVersion**](docs/Api/VersionApi.md#getversion) | **GET** /version | Get service version


## Documentation For Models

 - [AddOryAccessControlPolicyRoleMembers](docs/Model/AddOryAccessControlPolicyRoleMembers.md)
 - [AddOryAccessControlPolicyRoleMembersBody](docs/Model/AddOryAccessControlPolicyRoleMembersBody.md)
 - [AddOryAccessControlPolicyRoleMembersInternalServerError](docs/Model/AddOryAccessControlPolicyRoleMembersInternalServerError.md)
 - [AddOryAccessControlPolicyRoleMembersInternalServerErrorBody](docs/Model/AddOryAccessControlPolicyRoleMembersInternalServerErrorBody.md)
 - [AddOryAccessControlPolicyRoleMembersOK](docs/Model/AddOryAccessControlPolicyRoleMembersOK.md)
 - [AuthorizationResult](docs/Model/AuthorizationResult.md)
 - [DeleteOryAccessControlPolicy](docs/Model/DeleteOryAccessControlPolicy.md)
 - [DeleteOryAccessControlPolicyInternalServerError](docs/Model/DeleteOryAccessControlPolicyInternalServerError.md)
 - [DeleteOryAccessControlPolicyInternalServerErrorBody](docs/Model/DeleteOryAccessControlPolicyInternalServerErrorBody.md)
 - [DeleteOryAccessControlPolicyRole](docs/Model/DeleteOryAccessControlPolicyRole.md)
 - [DeleteOryAccessControlPolicyRoleInternalServerError](docs/Model/DeleteOryAccessControlPolicyRoleInternalServerError.md)
 - [DeleteOryAccessControlPolicyRoleInternalServerErrorBody](docs/Model/DeleteOryAccessControlPolicyRoleInternalServerErrorBody.md)
 - [DoOryAccessControlPoliciesAllow](docs/Model/DoOryAccessControlPoliciesAllow.md)
 - [DoOryAccessControlPoliciesAllowForbidden](docs/Model/DoOryAccessControlPoliciesAllowForbidden.md)
 - [DoOryAccessControlPoliciesAllowInternalServerError](docs/Model/DoOryAccessControlPoliciesAllowInternalServerError.md)
 - [DoOryAccessControlPoliciesAllowInternalServerErrorBody](docs/Model/DoOryAccessControlPoliciesAllowInternalServerErrorBody.md)
 - [DoOryAccessControlPoliciesAllowOK](docs/Model/DoOryAccessControlPoliciesAllowOK.md)
 - [GetOryAccessControlPolicy](docs/Model/GetOryAccessControlPolicy.md)
 - [GetOryAccessControlPolicyInternalServerError](docs/Model/GetOryAccessControlPolicyInternalServerError.md)
 - [GetOryAccessControlPolicyInternalServerErrorBody](docs/Model/GetOryAccessControlPolicyInternalServerErrorBody.md)
 - [GetOryAccessControlPolicyNotFound](docs/Model/GetOryAccessControlPolicyNotFound.md)
 - [GetOryAccessControlPolicyNotFoundBody](docs/Model/GetOryAccessControlPolicyNotFoundBody.md)
 - [GetOryAccessControlPolicyOK](docs/Model/GetOryAccessControlPolicyOK.md)
 - [GetOryAccessControlPolicyRole](docs/Model/GetOryAccessControlPolicyRole.md)
 - [GetOryAccessControlPolicyRoleInternalServerError](docs/Model/GetOryAccessControlPolicyRoleInternalServerError.md)
 - [GetOryAccessControlPolicyRoleInternalServerErrorBody](docs/Model/GetOryAccessControlPolicyRoleInternalServerErrorBody.md)
 - [GetOryAccessControlPolicyRoleNotFound](docs/Model/GetOryAccessControlPolicyRoleNotFound.md)
 - [GetOryAccessControlPolicyRoleNotFoundBody](docs/Model/GetOryAccessControlPolicyRoleNotFoundBody.md)
 - [GetOryAccessControlPolicyRoleOK](docs/Model/GetOryAccessControlPolicyRoleOK.md)
 - [HealthNotReadyStatus](docs/Model/HealthNotReadyStatus.md)
 - [HealthStatus](docs/Model/HealthStatus.md)
 - [InlineResponse500](docs/Model/InlineResponse500.md)
 - [Input](docs/Model/Input.md)
 - [IsInstanceAliveInternalServerError](docs/Model/IsInstanceAliveInternalServerError.md)
 - [IsInstanceAliveInternalServerErrorBody](docs/Model/IsInstanceAliveInternalServerErrorBody.md)
 - [IsInstanceAliveOK](docs/Model/IsInstanceAliveOK.md)
 - [ListOryAccessControlPolicies](docs/Model/ListOryAccessControlPolicies.md)
 - [ListOryAccessControlPoliciesInternalServerError](docs/Model/ListOryAccessControlPoliciesInternalServerError.md)
 - [ListOryAccessControlPoliciesInternalServerErrorBody](docs/Model/ListOryAccessControlPoliciesInternalServerErrorBody.md)
 - [ListOryAccessControlPoliciesOK](docs/Model/ListOryAccessControlPoliciesOK.md)
 - [ListOryAccessControlPolicyRoles](docs/Model/ListOryAccessControlPolicyRoles.md)
 - [ListOryAccessControlPolicyRolesInternalServerError](docs/Model/ListOryAccessControlPolicyRolesInternalServerError.md)
 - [ListOryAccessControlPolicyRolesInternalServerErrorBody](docs/Model/ListOryAccessControlPolicyRolesInternalServerErrorBody.md)
 - [ListOryAccessControlPolicyRolesOK](docs/Model/ListOryAccessControlPolicyRolesOK.md)
 - [OryAccessControlPolicies](docs/Model/OryAccessControlPolicies.md)
 - [OryAccessControlPolicy](docs/Model/OryAccessControlPolicy.md)
 - [OryAccessControlPolicyAllowedInput](docs/Model/OryAccessControlPolicyAllowedInput.md)
 - [OryAccessControlPolicyRole](docs/Model/OryAccessControlPolicyRole.md)
 - [OryAccessControlPolicyRoles](docs/Model/OryAccessControlPolicyRoles.md)
 - [Policy](docs/Model/Policy.md)
 - [RemoveOryAccessControlPolicyRoleMembers](docs/Model/RemoveOryAccessControlPolicyRoleMembers.md)
 - [RemoveOryAccessControlPolicyRoleMembersInternalServerError](docs/Model/RemoveOryAccessControlPolicyRoleMembersInternalServerError.md)
 - [RemoveOryAccessControlPolicyRoleMembersInternalServerErrorBody](docs/Model/RemoveOryAccessControlPolicyRoleMembersInternalServerErrorBody.md)
 - [Role](docs/Model/Role.md)
 - [SwaggerHealthStatus](docs/Model/SwaggerHealthStatus.md)
 - [SwaggerNotReadyStatus](docs/Model/SwaggerNotReadyStatus.md)
 - [SwaggerVersion](docs/Model/SwaggerVersion.md)
 - [UpsertOryAccessControlPolicy](docs/Model/UpsertOryAccessControlPolicy.md)
 - [UpsertOryAccessControlPolicyInternalServerError](docs/Model/UpsertOryAccessControlPolicyInternalServerError.md)
 - [UpsertOryAccessControlPolicyInternalServerErrorBody](docs/Model/UpsertOryAccessControlPolicyInternalServerErrorBody.md)
 - [UpsertOryAccessControlPolicyOK](docs/Model/UpsertOryAccessControlPolicyOK.md)
 - [UpsertOryAccessControlPolicyRole](docs/Model/UpsertOryAccessControlPolicyRole.md)
 - [UpsertOryAccessControlPolicyRoleInternalServerError](docs/Model/UpsertOryAccessControlPolicyRoleInternalServerError.md)
 - [UpsertOryAccessControlPolicyRoleInternalServerErrorBody](docs/Model/UpsertOryAccessControlPolicyRoleInternalServerErrorBody.md)
 - [UpsertOryAccessControlPolicyRoleOK](docs/Model/UpsertOryAccessControlPolicyRoleOK.md)
 - [Version](docs/Model/Version.md)


## Documentation For Authorization

All endpoints do not require authorization.

## Author

hi@ory.sh

