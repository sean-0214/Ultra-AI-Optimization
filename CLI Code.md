Microsoft Windows [Version 10.0.22621.2715]
(c) Microsoft Corporation. All rights reserved.

C:\Users\sean0>cd C:\Users\sean0\serverless-route-optimization

C:\Users\sean0\serverless-route-optimization>sam build && sam deploy --guided
The resource AWS::Serverless::Function 'lambdaFunction' has specified S3 location for CodeUri. It will not be built and
SAM CLI does not support invoking it locally.
The resource AWS::Serverless::LayerVersion 'DependencyLayer' has specified S3 location for ContentUri. It will not be
built and SAM CLI does not support invoking it locally.

Build Succeeded

Built Artifacts  : .aws-sam\build
Built Template   : .aws-sam\build\template.yaml

Commands you can use next
=========================
[*] Validate SAM template: sam validate
[*] Invoke Function: sam local invoke
[*] Test Function in the Cloud: sam sync --stack-name {{stack-name}} --watch
[*] Deploy: sam deploy --guided

Configuring SAM deploy
======================

        Looking for config file [samconfig.toml] :  Found
        Reading default arguments  :  Success

        Setting default arguments for 'sam deploy'
        =========================================
        Stack Name [AWSMAP]: AWSMAP
        AWS Region [ap-southeast-1]: ap-southeast-1
        Parameter MapName [Cathaymap]: Cathaymap
        Parameter PlaceIndexName [CathayPlaceIndex]: CathayPlaceIndex
        Parameter RouteCalculatorName [RouteCalculatorName]: RouteCalculatorName
        Parameter lambdaFunctionName [CognitoAuthCathay]: CognitoAuthCathay
        Parameter CognitoAuthName [Cathaycognitoauth]: Cathaycognitoauth
        #Shows you resources changes to be deployed and require a 'Y' to initiate deploy
        Confirm changes before deploy [Y/n]: Y
        #SAM needs permission to be able to create roles to connect to the resources in your template
        Allow SAM CLI IAM role creation [Y/n]: Y
        #Preserves the state of previously provisioned resources when an operation fails
        Disable rollback [Y/n]: Y
The resource AWS::Serverless::Function 'lambdaFunction' has specified S3 location for CodeUri. It will not be built and
SAM CLI does not support invoking it locally.
        Save arguments to configuration file [Y/n]: Y
        SAM configuration file [samconfig.toml]:
        SAM configuration environment [default]:

        Looking for resources needed for deployment:

        Managed S3 bucket: aws-sam-cli-managed-default-samclisourcebucket-f9lndfhlfkuc
        A different default S3 bucket can be set in samconfig.toml and auto resolution of buckets turned off by setting resolve_s3=False

        Saved arguments to config file
        Running 'sam deploy' for future deployments will use the parameters saved above.
        The above parameters can be changed by modifying samconfig.toml
        Learn more about samconfig.toml syntax at
        https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-config.html


        Deploying with following values
        ===============================
        Stack name                   : AWSMAP
        Region                       : ap-southeast-1
        Confirm changeset            : True
        Disable rollback             : True
        Deployment s3 bucket         : aws-sam-cli-managed-default-samclisourcebucket-f9lndfhlfkuc
        Capabilities                 : ["CAPABILITY_IAM"]
        Parameter overrides          : {"MapName": "Cathaymap", "PlaceIndexName": "CathayPlaceIndex", "RouteCalculatorName": "RouteCalculatorName", "lambdaFunctionName": "CognitoAuthCathay", "CognitoAuthName": "Cathaycognitoauth"}
        Signing Profiles             : {}

Initiating deployment
=====================

        Uploading to AWSMAP/d848018fc5130b2de882f6077b5b45d2.template  5318 / 5318  (100.00%)


Waiting for changeset to be created..

CloudFormation stack changeset
---------------------------------------------------------------------------------------------------------------------
Operation                     LogicalResourceId             ResourceType
        Replacement
---------------------------------------------------------------------------------------------------------------------
+ Add                         DependencyLayer42039fb1f1     AWS::Lambda::LayerVersion     N/A
+ Add                         ServerlessRestApiDeployment   AWS::ApiGateway::Deployment   N/A
                              94fe84ca77

* Modify                      ServerlessRestApiProdStage    AWS::ApiGateway::Stage        False
* Modify                      ServerlessRestApi             AWS::ApiGateway::RestApi      False
* Modify                      lambdaApiGatewayInvoke        AWS::Lambda::Permission       True
* Modify                      lambdaFunctionAPIEventPermi   AWS::Lambda::Permission       True
                              ssionProd

* Modify                      lambdaFunction                AWS::Lambda::Function         True
- Delete                      DependencyLayer836d54c348     AWS::Lambda::LayerVersion     N/A
---------------------------------------------------------------------------------------------------------------------


Changeset created successfully. arn:aws:cloudformation:ap-southeast-1:298906653599:changeSet/samcli-deploy1700357617/d831aa70-918d-453a-83f4-f2269ec4e345


Previewing CloudFormation changeset before deployment
======================================================
Deploy this changeset? [y/N]: y

2023-11-19 09:36:29 - Waiting for stack create/update to complete

CloudFormation events from stack operations (refresh every 5.0 seconds)
---------------------------------------------------------------------------------------------------------------------
ResourceStatus                ResourceType                  LogicalResourceId             ResourceStatusReason
---------------------------------------------------------------------------------------------------------------------
UPDATE_IN_PROGRESS            AWS::CloudFormation::Stack    AWSMAP
        User Initiated
CREATE_IN_PROGRESS            AWS::Lambda::LayerVersion     DependencyLayer42039fb1f1     -
CREATE_IN_PROGRESS            AWS::Lambda::LayerVersion     DependencyLayer42039fb1f1     Resource creation Initiated
CREATE_COMPLETE               AWS::Lambda::LayerVersion     DependencyLayer42039fb1f1     -
UPDATE_FAILED                 AWS::Lambda::Function         lambdaFunction                Replacement type updates

        not supported on stack with

        disable-rollback.
UPDATE_IN_PROGRESS            AWS::CloudFormation::Stack    AWSMAP
        Replacement type updates

        not supported on stack with

        disable-rollback.
UPDATE_ROLLBACK_COMPLETE      AWS::Lambda::Function         lambdaFunction                Rollback succeeded for the

        failed resources.
UPDATE_FAILED                 AWS::CloudFormation::Stack    AWSMAP
        The following resource(s)

        failed to update:

        [lambdaFunction].
---------------------------------------------------------------------------------------------------------------------


Failed to deploy. Automatic rollback disabled for this deployment.

Actions you can take next
=========================
[*] Fix issues and try deploying again
[*] Roll back stack to the last known stable state: aws cloudformation
rollback-stack --stack-name AWSMAP

Error: Failed to create/update the stack: AWSMAP, Waiter StackUpdateComplete failed: Waiter encountered a terminal failure state: For expression "Stacks[].StackStatus" we matched expected path: "UPDATE_FAILED" at least once

C:\Users\sean0\serverless-route-optimization>sam deploy --guided

Configuring SAM deploy
======================

        Looking for config file [samconfig.toml] :  Found
        Reading default arguments  :  Success

        Setting default arguments for 'sam deploy'
        =========================================
        Stack Name [AWSMAP]: AWSMAP
        AWS Region [ap-southeast-1]: ap-southeast-1
        Parameter MapName [Cathaymap]: Cathaymap
        Parameter PlaceIndexName [CathayPlaceIndex]: CathayPlaceIndex
        Parameter RouteCalculatorName [RouteCalculatorName]: RouteCalculatorName
        Parameter lambdaFunctionName [CognitoAuthCathay]: CognitoAuthCathay
        Parameter CognitoAuthName [Cathaycognitoauth]: Cathaycognitoauth
        #Shows you resources changes to be deployed and require a 'Y' to initiate deploy
        Confirm changes before deploy [Y/n]: Y
        #SAM needs permission to be able to create roles to connect to the resources in your template
        Allow SAM CLI IAM role creation [Y/n]: Y
        #Preserves the state of previously provisioned resources when an operation fails
        Disable rollback [Y/n]: n
The resource AWS::Serverless::Function 'lambdaFunction' has specified S3 location
for CodeUri. It will not be built and SAM CLI does not support invoking it
locally.
        Save arguments to configuration file [Y/n]: Y
        SAM configuration file [samconfig.toml]:
        SAM configuration environment [default]:

        Looking for resources needed for deployment:

        Managed S3 bucket: aws-sam-cli-managed-default-samclisourcebucket-f9lndfhlfkuc
        A different default S3 bucket can be set in samconfig.toml and auto resolution of buckets turned off by setting resolve_s3=False

        Saved arguments to config file
        Running 'sam deploy' for future deployments will use the parameters saved above.
        The above parameters can be changed by modifying samconfig.toml
        Learn more about samconfig.toml syntax at
        https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-config.html


        Deploying with following values
        ===============================
        Stack name                   : AWSMAP
        Region                       : ap-southeast-1
        Confirm changeset            : True
        Disable rollback             : False
        Deployment s3 bucket         : aws-sam-cli-managed-default-samclisourcebucket-f9lndfhlfkuc
        Capabilities                 : ["CAPABILITY_IAM"]
        Parameter overrides          : {"MapName": "Cathaymap", "PlaceIndexName": "CathayPlaceIndex", "RouteCalculatorName": "RouteCalculatorName", "lambdaFunctionName": "CognitoAuthCathay", "CognitoAuthName": "Cathaycognitoauth"}
        Signing Profiles             : {}

Initiating deployment
=====================

File with same data already exists at
AWSMAP/d848018fc5130b2de882f6077b5b45d2.template, skipping upload


Waiting for changeset to be created..

CloudFormation stack changeset
-------------------------------------------------------------------------------------------------
Operation                LogicalResourceId        ResourceType             Replacement
-------------------------------------------------------------------------------------------------
+ Add                    ServerlessRestApiDeplo   AWS::ApiGateway::Deplo   N/A

                         yment94fe84ca77          yment

* Modify                 ServerlessRestApiProdS   AWS::ApiGateway::Stage   False

                         tage

* Modify                 ServerlessRestApi        AWS::ApiGateway::RestA   False

                                                  pi

* Modify                 lambdaApiGatewayInvoke   AWS::Lambda::Permissio   True

                                                  n

* Modify                 lambdaFunctionAPIEvent   AWS::Lambda::Permissio   True

                         PermissionProd           n

* Modify                 lambdaFunctionRole       AWS::IAM::Role           False

* Modify                 lambdaFunction           AWS::Lambda::Function    True

* Modify                 lambdaLogGroup           AWS::Logs::LogGroup      True

-------------------------------------------------------------------------------------------------


Changeset created successfully. arn:aws:cloudformation:ap-southeast-1:298906653599:changeSet/samcli-deploy1700360750/5cc6bfc6-6a84-4834-9f4f-7c0154cef26c


Previewing CloudFormation changeset before deployment
======================================================
Deploy this changeset? [y/N]: y
Error: Failed to create/update the stack: AWSMAP, An error occurred (ValidationError) when calling the ExecuteChangeSet operation: This stack is currently in a non-terminal [UPDATE_FAILED] state. To update the stack from this state, please use the disable-rollback parameter with update-stack API. To rollback to the last known good state, use the rollback-stack API

C:\Users\sean0\serverless-route-optimization>sam deploy --guided

Configuring SAM deploy
======================

        Looking for config file [samconfig.toml] :  Found
        Reading default arguments  :  Success

        Setting default arguments for 'sam deploy'
        =========================================
        Stack Name [AWSMAP]: AWSMAP
        AWS Region [ap-southeast-1]: ap-southeast-1
        Parameter MapName [Cathaymap]: Cathaymap
        Parameter PlaceIndexName [CathayPlaceIndex]: CathayPlaceIndex
        Parameter RouteCalculatorName [RouteCalculatorName]: RouteCalculatorName
        Parameter lambdaFunctionName [CognitoAuthCathay]: CognitoAuthCathay
        Parameter CognitoAuthName [Cathaycognitoauth]: Cathaycognitoauth
        #Shows you resources changes to be deployed and require a 'Y' to initiate deploy
        Confirm changes before deploy [Y/n]: Y
        #SAM needs permission to be able to create roles to connect to the resources in your template
        Allow SAM CLI IAM role creation [Y/n]: Y
        #Preserves the state of previously provisioned resources when an operation fails
        Disable rollback [Y/n]: Y
The resource AWS::Serverless::Function 'lambdaFunction' has specified S3 location
for CodeUri. It will not be built and SAM CLI does not support invoking it
locally.
        Save arguments to configuration file [Y/n]: Y
        SAM configuration file [samconfig.toml]:
        SAM configuration environment [default]:

        Looking for resources needed for deployment:

        Managed S3 bucket: aws-sam-cli-managed-default-samclisourcebucket-f9lndfhlfkuc
        A different default S3 bucket can be set in samconfig.toml and auto resolution of buckets turned off by setting resolve_s3=False

        Saved arguments to config file
        Running 'sam deploy' for future deployments will use the parameters saved above.
        The above parameters can be changed by modifying samconfig.toml
        Learn more about samconfig.toml syntax at
        https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-config.html


        Deploying with following values
        ===============================
        Stack name                   : AWSMAP
        Region                       : ap-southeast-1
        Confirm changeset            : True
        Disable rollback             : True
        Deployment s3 bucket         : aws-sam-cli-managed-default-samclisourcebucket-f9lndfhlfkuc
        Capabilities                 : ["CAPABILITY_IAM"]
        Parameter overrides          : {"MapName": "Cathaymap", "PlaceIndexName": "CathayPlaceIndex", "RouteCalculatorName": "RouteCalculatorName", "lambdaFunctionName": "CognitoAuthCathay", "CognitoAuthName": "Cathaycognitoauth"}
        Signing Profiles             : {}

Initiating deployment
=====================

File with same data already exists at
AWSMAP/d848018fc5130b2de882f6077b5b45d2.template, skipping upload


Waiting for changeset to be created..

CloudFormation stack changeset
-------------------------------------------------------------------------------------------------
Operation                LogicalResourceId        ResourceType             Replacement
-------------------------------------------------------------------------------------------------
+ Add                    AmazonLocationMap        AWS::Location::Map       N/A

+ Add                    AmazonLocationPlaceInd   AWS::Location::PlaceIn   N/A

                         ex                       dex

+ Add                    AmazonLocationRouteCal   AWS::Location::RouteCa   N/A

                         culator                  lculator

+ Add                    DependencyLayer42039fb   AWS::Lambda::LayerVers   N/A

                         1f1                      ion

+ Add                    IamRole                  AWS::IAM::Role           N/A

+ Add                    ServerlessRestApiDeplo   AWS::ApiGateway::Deplo   N/A

                         yment94fe84ca77          yment

+ Add                    ServerlessRestApiProdS   AWS::ApiGateway::Stage   N/A

                         tage

+ Add                    ServerlessRestApi        AWS::ApiGateway::RestA   N/A

                                                  pi

+ Add                    identityPoolRole         AWS::Cognito::Identity   N/A

                                                  PoolRoleAttachment

+ Add                    identityPool             AWS::Cognito::Identity   N/A

                                                  Pool

+ Add                    lambdaApiGatewayInvoke   AWS::Lambda::Permissio   N/A

                                                  n

+ Add                    lambdaFunctionAPIEvent   AWS::Lambda::Permissio   N/A

                         PermissionProd           n

+ Add                    lambdaFunctionRole       AWS::IAM::Role           N/A

+ Add                    lambdaFunction           AWS::Lambda::Function    N/A

+ Add                    lambdaLogGroup           AWS::Logs::LogGroup      N/A

-------------------------------------------------------------------------------------------------


Changeset created successfully. arn:aws:cloudformation:ap-southeast-1:298906653599:changeSet/samcli-deploy1700361024/d6383aab-acfd-43bc-88ef-f6ef6700dba9


Previewing CloudFormation changeset before deployment
======================================================
Deploy this changeset? [y/N]: y

2023-11-19 10:30:33 - Waiting for stack create/update to complete

CloudFormation events from stack operations (refresh every 5.0 seconds)
-------------------------------------------------------------------------------------------------
ResourceStatus           ResourceType             LogicalResourceId        ResourceStatusReason
-------------------------------------------------------------------------------------------------
CREATE_IN_PROGRESS       AWS::CloudFormation::S   AWSMAP                   User Initiated
                         tack

CREATE_IN_PROGRESS       AWS::IAM::Role           lambdaFunctionRole       -

CREATE_IN_PROGRESS       AWS::Location::PlaceIn   AmazonLocationPlaceInd   -

                         dex                      ex

CREATE_IN_PROGRESS       AWS::Lambda::LayerVers   DependencyLayer42039fb   -

                         ion                      1f1

CREATE_IN_PROGRESS       AWS::Location::RouteCa   AmazonLocationRouteCal   -

                         lculator                 culator

CREATE_IN_PROGRESS       AWS::Logs::LogGroup      lambdaLogGroup           -

CREATE_IN_PROGRESS       AWS::Cognito::Identity   identityPool             -

                         Pool

CREATE_IN_PROGRESS       AWS::Location::Map       AmazonLocationMap        -

CREATE_IN_PROGRESS       AWS::Location::RouteCa   AmazonLocationRouteCal   Resource creation
                         lculator                 culator                  Initiated
CREATE_IN_PROGRESS       AWS::Logs::LogGroup      lambdaLogGroup           Resource creation
                                                                           Initiated
CREATE_IN_PROGRESS       AWS::Cognito::Identity   identityPool             Resource creation
                         Pool                                              Initiated
CREATE_IN_PROGRESS       AWS::Location::PlaceIn   AmazonLocationPlaceInd   Resource creation
                         dex                      ex                       Initiated
CREATE_COMPLETE          AWS::Location::RouteCa   AmazonLocationRouteCal   -

                         lculator                 culator

CREATE_IN_PROGRESS       AWS::Location::Map       AmazonLocationMap        Resource creation
                                                                           Initiated
CREATE_COMPLETE          AWS::Logs::LogGroup      lambdaLogGroup           -

CREATE_COMPLETE          AWS::Location::PlaceIn   AmazonLocationPlaceInd   -

                         dex                      ex

CREATE_COMPLETE          AWS::Location::Map       AmazonLocationMap        -

CREATE_COMPLETE          AWS::Cognito::Identity   identityPool             -

                         Pool

CREATE_IN_PROGRESS       AWS::IAM::Role           lambdaFunctionRole       Resource creation
                                                                           Initiated
CREATE_IN_PROGRESS       AWS::IAM::Role           IamRole                  -

CREATE_IN_PROGRESS       AWS::IAM::Role           IamRole                  Resource creation
                                                                           Initiated
CREATE_IN_PROGRESS       AWS::Lambda::LayerVers   DependencyLayer42039fb   Resource creation
                         ion                      1f1                      Initiated
CREATE_COMPLETE          AWS::Lambda::LayerVers   DependencyLayer42039fb   -

                         ion                      1f1

CREATE_COMPLETE          AWS::IAM::Role           lambdaFunctionRole       -

CREATE_COMPLETE          AWS::IAM::Role           IamRole                  -

CREATE_IN_PROGRESS       AWS::Lambda::Function    lambdaFunction           -

CREATE_IN_PROGRESS       AWS::Lambda::Function    lambdaFunction           Resource creation
                                                                           Initiated
CREATE_IN_PROGRESS       AWS::Cognito::Identity   identityPoolRole         -

                         PoolRoleAttachment

CREATE_IN_PROGRESS       AWS::Cognito::Identity   identityPoolRole         Resource creation
                         PoolRoleAttachment                                Initiated
CREATE_COMPLETE          AWS::Cognito::Identity   identityPoolRole         -

                         PoolRoleAttachment

CREATE_COMPLETE          AWS::Lambda::Function    lambdaFunction           -

CREATE_IN_PROGRESS       AWS::Lambda::Permissio   lambdaApiGatewayInvoke   -

                         n

CREATE_IN_PROGRESS       AWS::ApiGateway::RestA   ServerlessRestApi        -

                         pi

CREATE_IN_PROGRESS       AWS::Lambda::Permissio   lambdaApiGatewayInvoke   Resource creation
                         n                                                 Initiated
CREATE_COMPLETE          AWS::Lambda::Permissio   lambdaApiGatewayInvoke   -

                         n

CREATE_IN_PROGRESS       AWS::ApiGateway::RestA   ServerlessRestApi        Resource creation
                         pi                                                Initiated
CREATE_COMPLETE          AWS::ApiGateway::RestA   ServerlessRestApi        -

                         pi

CREATE_IN_PROGRESS       AWS::Lambda::Permissio   lambdaFunctionAPIEvent   -

                         n                        PermissionProd

CREATE_IN_PROGRESS       AWS::ApiGateway::Deplo   ServerlessRestApiDeplo   -

                         yment                    yment94fe84ca77

CREATE_IN_PROGRESS       AWS::Lambda::Permissio   lambdaFunctionAPIEvent   Resource creation
                         n                        PermissionProd           Initiated
CREATE_COMPLETE          AWS::Lambda::Permissio   lambdaFunctionAPIEvent   -

                         n                        PermissionProd

CREATE_IN_PROGRESS       AWS::ApiGateway::Deplo   ServerlessRestApiDeplo   Resource creation
                         yment                    yment94fe84ca77          Initiated
CREATE_COMPLETE          AWS::ApiGateway::Deplo   ServerlessRestApiDeplo   -

                         yment                    yment94fe84ca77

CREATE_IN_PROGRESS       AWS::ApiGateway::Stage   ServerlessRestApiProdS   -

                                                  tage

CREATE_IN_PROGRESS       AWS::ApiGateway::Stage   ServerlessRestApiProdS   Resource creation
                                                  tage                     Initiated
CREATE_COMPLETE          AWS::ApiGateway::Stage   ServerlessRestApiProdS   -

                                                  tage

CREATE_COMPLETE          AWS::CloudFormation::S   AWSMAP                   -

                         tack

-------------------------------------------------------------------------------------------------

CloudFormation outputs from deployed stack
-------------------------------------------------------------------------------------------------
Outputs

-------------------------------------------------------------------------------------------------
Key                 ApiGatewayInvokeURL

Description         -

Value               https://v65eop68m1.execute-api.ap-southeast-1.amazonaws.com/Prod/

Key                 MapName

Description         -

Value               Cathaymap


Key                 Region

Description         -

Value               ap-southeast-1


Key                 identityPoolId

Description         -

Value               ap-southeast-1:09655d24-f338-47ff-bc01-4bfa9c9e9b65

-------------------------------------------------------------------------------------------------


Successfully created/updated stack - AWSMAP in ap-southeast-1


C:\Users\sean0\serverless-route-optimization>^A
