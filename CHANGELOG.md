## 1.21.3.0 (2021-07-28)

- **Bug Fix** Fixed issue in the Create/Edit Profile dialog box where importing from a CSV file would not update the UI.
- **Bug Fix** Lambda Test tool is now set up when Visual Studio launches and immediately loads a solution
- **Deprecation** Removed the nodejs8.10 runtime from Lambda deployment dialogs. This runtime has reached end of support. See https://docs.aws.amazon.com/lambda/latest/dg/runtime-support-policy.html for more details.
- **Feature** The Toolkit's User Guide can now be accessed from the "AWS Toolkit" menu, located in the "Extensions" menu ("Tools" menu in Visual Studio 2017)
- **Feature** Added a menu item to report a bug or make a feature request, available from the "AWS Toolkit" menu, located in the "Extensions" menu ("Tools" menu in Visual Studio 2017)

## 1.21.2.0 (2021-05-20)

- **Bug Fix** Fixed an issue where the toolkit had initialization failures when the development environment did not have access to Windows Encrypted Store.
- **Bug Fix** The EC2 Quick Launch dialog dropdowns for Security Group and IAM Role are now sorted.
- **Bug Fix** IAM Role Dropdowns in the deployment dialogs for Lambda and ECS are now sorted.
- **Bug Fix** Fixed an issue introduced in the previous version where the Toolkit was unable to resolve SAML based profiles.

## 1.21.1.0 (2021-04-23)

- **Bug Fix** Fixed an issue introduced in the previous version where TeamExplorer events were excessively written to the Toolkit log
- **Bug Fix** Fixed an issue where the toolkit would fail to start when the Shared Credentials file directory "%USERPROFILE%/.aws" was absent. The toolkit now creates the directory if absent on startup.
- **Feature** For performance reasons, the AWS Explorer no longer automatically connects to credential_process based credentials on startup. Instead, a link to log in is shown in the AWS Explorer.

## 1.21.0.0 (2021-04-21)

- **Breaking Change** Support for working in region sets (aka Partitions) like GovCloud or China has changed. If your account is based in a different partition (like GovCloud or China), you will need to set the `region` field in your credentials profile so that the Toolkit is able to work with the proper set of regions. Previously, this was adjusted using the 'Account Type' field in the add/edit Profile dialog.
- **Breaking Change** A change was made to the way the Toolkit records which account is used by the AWS Explorer. The first time you launch the Toolkit after updating, the AWS Explorer will not automatically select the account you used previously.
- **Feature** Added support for AWS SSO based credential profiles. Selecting credentials based on AWS SSO will open a prompt to launch a browser-based SSO Login.
- **Feature** Added support for credential profiles that assume a role and use MFA. Selecting credentials that use MFA will prompt for an MFA code.
- **Feature** The Toolkit makes a validation check when changing the currently active credentials and region. Validation messages are shown while a validation is in progress, and if the validation check fails.
- **Feature** When credentials profiles are loaded by the Toolkit, the Output pane indicates how many profiles were loaded, and which profiles are unsupported/invalid. The Toolkit logs contain details to diagnose why a profile cannot be used.
- **Feature** The Toolkit now shows all supported credential profiles in the AWS Explorer. Previously, the Toolkit would list a subset of credentials based on a de-duplication of the access key.

## 1.20.2.0 (2021-04-07)

- **Bug Fix** Improved the legibility of the Template tab in the CloudFormation stack viewer
- **Bug Fix** Fixed issue where yaml based CloudFormation templates could not be deployed when they contained short form notation
- **Bug Fix** Fixed issue where CloudFormation Stacks could not be viewed from AWS Explorer when they contained yaml short form notation
- **Deprecation** IAM Roles created when deploying to Beanstalk will now reference the managed policy AWSElasticBeanstalkManagedUpdatesCustomerRolePolicy instead of AWSElasticBeanstalkService, which is deprecated. Users are encouraged to update any roles having the deprecated managed policy AWSElasticBeanstalkService. For more information, please see - https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/security-iam-awsmanpol.html
- **Feature** Source account is now included in the resource policy when creating event notifications for S3 buckets.
- **Removal** Removed optional account number field from credential profile dialogs.

## 1.20.1.0 (2021-01-21)

- **Bug Fix** Fixed ECS Cluster View Panel to show scheduled tasks registered with the cluster being viewed.
- **Bug Fix** Fixed issue where incorrect tag value was saved in the defaults file when Docker Repository name contained a `/`
- **Deprecation** Updated all references of the deprecated AWSLambdaFullAccess and AWSLambdaReadOnlyAccess managed policies to AWSLambda_FullAccess and AWSLambda_ReadOnlyAccess.
- **Feature** Upload Lambda Function dialog now filters the existing function list based on selected package type.
- **Feature** Source account is now included in the event source policy when creating S3 event sources for Lambda functions.
- **Feature** Added ability in Publish Container to AWS wizard to load previous deployment settings stored in aws-ecs-tools-defaults.json 
- **Feature** Added support to deploy fargate based scheduled tasks on ECS cluster.

## 1.20.0.0 (2020-12-01)

- **Feature** Container Image Support in Lambda: A new Lambda Project is available to create Image based Lambda functions (Visual Studio 2019 only)
- **Feature** Container Image Support in Lambda: Deploy Image-based Lambda functions to AWS Lambda
- **Feature** Added .NET Lambda Test Tool support for .NET 5 Lambda function projects

## 1.19.0.0 (2020-11-23)

- **Bug Fix** The AWS .NET Mock Lambda Test Tool is now configured in launchSettings.json with a location based on %USERPROFILE% instead of %USERNAME%
- **Feature** Improved solution load times by only installing the Lambda Test tool once per IDE session instead of once per applicable project.
- **Feature** Lambda Function View Panel now shows function's state and last updated status.
- **Feature** Added AWS CodeArtifact in AWS Explorer with option to copy NuGet source endpoint. Added NuGet Credential Provider for CodeArtifact.

## 1.18.1.0 (2020-07-23)

-   Fixed "security group does not exist" issue when deploying .NET Core applications to Beanstalk that use an RDS security group
-   Fixed an issue where Beanstalk deployments can fail if the host Windows system is using non-US regional format settings
-   Fixed an issue where nodejs Lambda deployments can fail if the host Windows system is using non-US regional format settings
-   Fixed issue where certain error messages pop "under" other windows, and are not properly modal

## 1.18.0.0 (2020-06-23)

-   Added support to publish ASP.NET Core applications to the new ".NET Core on Linux" Beanstalk platform.
-   A banner is shown on first usage, indicating that information relating to Toolkit usage is collected.
-   Fixed an issue where first-time users of the Toolkit were not being shown the "Getting Started" dialog in Visual Studio 2019. All users will see this dialog the first time Visual Studio is opened after installing this version of the toolkit.
-   Fixed an issue where the Toolkit-generated Beanstalk service role (aws-elasticbeanstalk-service-role) causes Beanstalk deployments to report a RED health status when they use multi-instance Application Load Balancers. Whenever the role is created, a service policy is now attached to it.
-   Fixed an issue where the Beanstalk deployment wizard would not populate roles on the Permissions page when trying to deploy to certain regions.
-   Removed the option to save Beanstalk configurations out to the old awsdeploy tool (awsdeploy.exe). This tool has been succeeded by the dotnet CLI tools package "Amazon.ElasticBeanstalk.Tools".

## 1.17.1.0 (2020-04-22)

-   Fixed an issue where subnet and security groups would not show when viewing a Lambda Function.
-   Fixed an issue on toolkit startup that caused the following message to appear in Activity Log: SetSite failed for package AWSToolkitPackage Source: 'EnvDTE' ... EnvDTE.Events.get_DebuggerEvents
-   Fixed an issue where CodeCommit repos would not appear if the account did not have access permissions to all of them.
-   Fix dark theme support in the Beanstalk Advanced pane for Custom Availability Zones.
-   The Toolkit's welcome panel now has scroll bars that appear when the contents don't all fit in the view.
-   Improvements to the toolkits startup performance.

## 1.17.0.0 (2020-03-31)

-   Added support .NET Core 3.1 Lambda support.
-   Fixed some issues where a "File is already open" error would appear in versions of Visual Studio 2019 16.5 and newer.
-   Added ability to right click deploy a serverless.template as a solution item.
-   Removed configuration and target framework from serverless deployment wizard as those sittings are inferred from the project being deployed.
-   Improvements to the Context Menu for S3 items in the AWS Explorer
-   Improvements to the toolkits startup performance.
-   Fixed issue with content type not being set for JSON files uploaded to S3 in the S3 browser.
-   Updated the toolkit to use the latest version of the AWS SDK for .NET.

## 1.16.1.0 (2020-02-19)

-   Elastic Beanstalk launch wizard now shows subnet tags alongside VPC options
-   RDS launch wizard now auto-selects the default subnet group
-   Checkboxes and radio buttons that are disabled are now appropriately greyed out
-   Fixed issue where trying to Show/Hide columns in some views would crash Visual Studio
-   Fixed issue related to setting health check URLs on Beanstalk environments that use ALBs
-   The RDS Launch wizard no longer shows database engines that the wizard doesn't provide support for
-   Fixed issue with RDS Launch Wizard not correctly enabling the Next and Finish buttons in the advanced page
-   Fixed issue with Add to Server Explorer not working from the RDS Instance view

## 1.16.0.0 (2020-02-06)

-   Add ability in Elastic Beanstalk deployment wizard to select the type of Elastic Load Balancer to use.
-   Updated the Elastic Beanstalk deployment wizard to allow selecting multiple subnets.
-   Add Node.js 12 as a Lambda deployment option.
-   Updated the available storage class that can be assigned to S3 objects in the S3 bucket browser.
-   Updated CloudFormation stack view to show the URL if the stack contained an API Gateway HTTP API.
-   Fixed issue with using the correct IAM endpoint when using the me-south-1 region.
-   Updated the toolkit to use the latest version of the AWS SDK for .NET.
-   Updated the Lambda new project wizard to have VS 2017 and 2019 pull available blueprints from a separate source.
-   Updated feature that configures the Lambda Test Tool to use %USERNAME% when setting up the executablePath in launchSettings.json.

## 1.15.2.1 (2019-07-02)

-   Fix issue with file locking issues when listening to file changes to the shared credentials file.

## 1.15.2.0 (2019-05-23)

-   Fix issue with CodeCommit not working correct in VS 2019.
-   Update Project Templates to support VS 2019 filtering.
-   Provide option to save a profile in the shard credentials file.
-   Update Lambda deployment code from "dotnet lambda" cli which contains customer fix for the error message "The filename or extension is too long".

## 1.15.1.0 (2019-04-17)

-   Fix issue with CodeCommit not working correct in VS 2017.
-   Remove ASP.NET Core version check.
-   Pull in latest changes of Amazon.Lambda.Tools for Lambda deployment.

## 1.15.0.0 (2019-03-28)

-   Add support or Visual Studio 2019
-   Add support for Lambda Custom Runtime deployment.
-   Add support for Lambda Layers during deployment.
-   Fixed bug where Lambda projects in a Project Folder were not detected for configuring .NET Lambda Test Tool.
-   Remove flag from region picker.
-   Fixed situation where a corrupt credentials file would crash VS on startup.
-   Updated Toolkit's Lambda Max Timeout to 900 seconds.
-   Pull in latest changes of Amazon.Lambda.Tools for Lambda deployment.

## 1.14.5.0 (2018-11-19)

-   Added ability to .NET Lambda Test Tool for opened Lambda projects.
-   Cosmetic UI changes to the Lambda function view.

## 1.14.4.0 (2018-07-09)

-   Added support for .NET Core 2.1 with AWS Lambda.
-   Added support for configuring SQS event source for AWS Lambda functions.
-   Added ability to set working directory for the docker build command in Amazon ECS deployment wizard.

## 1.14.3.3 (2018-05-24)

-   Fixed issue with Node.js AWS Lambda deployments incorrectly requiring a dead letter queue.

## 1.14.3.2 (2018-05-09)

-   Fixed issue deploying .NET Core 1.0 Lambda functions from within Visual Studio 2015 and 2017.

## 1.14.3.0 (2018-05-03)

-   Added F# AWS Lambda project templates.
-   Added Node.js 8.10 runtime enumeration when deploying Node.js AWS Lambda functions.
-   Added Lambda monitoring graphs to the CloudFormation stack view.
-   Fixed the serverless.template added to projects via "Add New Items -> Add Serverless Template" menu item to use dotnetcore2.0 runtime.

## 1.14.2.0 (2018-03-26)

-   Earlier versions of the AWS Toolkit with Visual Studio added additional AWS Lambda service accounts to the trust policy that are no longer used
    for IAM roles created as part of a Lambda deployment. A new prompt has been added when the role is selected in the Lambda deployment wizard to offer removing those accounts.
-   Sorted Linux AMIs in quick launch EC2 launch wizard to put the new .NET Core based AMI on top.
-   Fixed issue of showing ECS Service load balancer URL before the load balancer was active. If the link was clicked before it was active it could cause a bad DNS entry to be cached on the local system.
-   Fixed issue with Launch button being enabled before security group was selected in EC2 Launch wizard.

## 1.14.1.6 (2018-03-02)

-   Updated Elastic Beanstalk deployments to work around issue with including Roslyn folder in the deployment package for projects dependent on an v1.0.7 of the Microsoft.CodeDom.Providers.DotNetCompilerPlatform
    NuGet package.
-   Updated toolkit to use embedded resources for various metadata files if it cannot reach the online versions.
-   Updated ECS support to better detect when the Docker build needs to be run from the solution.
-   Fixed ECS tools to not report deployment error when deploying to a new cluster that has the same name as one recently deleted.
-   Fixed ECS tools to not persist the full URL of the image when saving the deployment settings.
-   Fixed ECS tools to set target type to 'Ip' on the ELB target group for Fargate deployments.
-   Fixed 'must reference a valid S3 object' error in CloudFormation deployment.

## 1.14.1.3 (2018-02-14)

-   Updated deployment to AWS Elastic Beanstalk to test if the target environment or solution stack supports the AWS X-Ray configuration options before adding them to the deployment request. This fixes issues with re-deployment using the latest wizard to environments running in older solution stacks. The wizard will show the X-Ray tracing option (if the region being deployed to supports X-Ray) but will ignore the option setting if the stack cannot support it.

## 1.14.1.2 (2018-02-12)

-   Updated the AWS Lambda and AWS Elastic Beanstalk deployment wizards to not show options to toggle X-Ray support when used in regions where AWS X-Ray is not yet available.

## 1.14.1.0 (2018-02-05)

-   Updated AWS Elastic Beanstalk deployment wizard to allow enabling application tracing with AWS X-Ray.
-   Updated AWS Lambda deployment wizard to allow enabling application tracing with AWS X-Ray.

## 1.14.0.1 (2018-01-22)

-   Fixed issue with the RDS Launch Instance wizard not showing all database engine types for an account.
-   Fixed issue with toolkit not setting CAPABILITY_NAMED_IAM when updating a stack.

## 1.14.0.0 (2018-01-15)

-   Added support for .NET Core 2.0 runtime for AWS Lambda in Visual Studio 2017.

## 1.13.0.6 (2017-12-28)

-   Fixed issue with trust policy for IAM Role when created for a Lambda function upload.

## 1.13.0.0 (2017-12-01)

-   New Amazon ECS Container deployment features for VS 2017.

## 1.12.2.1 (2017-10-12)

-   Fixed issue with deploying to AWS Lambda in US GovCloud region.

## 1.12.2.0 (2017-09-21)

-   Added support for deploying YAML based CloudFormation and Serverless templates.

## 1.12.1.5 (2017-08-16)

-   Corrected some minor theming issues.

## 1.12.1.4 (2017-08-14)

-   Updated the New Project templates for AWS in Visual Studio 2017 to use NuGet to reference assemblies from the AWS SDK for .NET and to fix some project incompatibilities.

## 1.12.1.3 (2017-08-07)

-   Updated the Microsoft.VisualStudio.MPF dependency from 11.0 to 15.0, matching the IDE version, to resolve install issue for some users.

## 1.12.1.2 (2017-07-27)

-   Fixed error when selecting AWS CodeCommit repository to clone if more than 25 repositories existed in a region for the user.

## 1.12.1.1 (2017-06-02)

-   Fixed issue with parsing duplicate keys in the shared credentials file.
-   Fixed syntax highlighting in the CloudFormation editor for custom resources and intrinsic functions.

## 1.12.1.0 (2017-06-01)

-   The toolkit is now generally available (GA) for Visual Studio 2017 editions in the Visual Studio Marketplace, https://marketplace.visualstudio.com/items?itemName=AmazonWebServices.AWSToolkitforVisualStudio2017.
-   Fixed issue with dead letter queue configuration getting cleared during redeploy of AWS Lambda functions.

## 1.11.7.6 (2017-05-16)

-   Fixed issue with crash when importing CSV file containing credentials that did not contain the correct column headers or was otherwise corrupt.

## 1.11.7.5 (2017-05-09)

-   Minor labelling and other UI changes for the AWS CodeCommit support.
-   Create CodeCommit repository now validates that the chosen name is available before leaving the dialog.

## 1.11.7.4 (2017-05-05)

-   Fixed issue with AWS Elastic Beanstalk deployments when using profiles from the shared credential file.
-   Added the ability to sort and order AWS CodeCommit repositories when selecting the repository to clone from within Team Explorer.

## 1.11.7.3 (2017-04-27)

-   Fixed issue in AWS Lambda deployment wizard not displaying all of the existing IAM roles and Lambda functions.

## 1.11.7.2 (2017-04-24)

-   Added validation to stop publishing .NET Core 1.0 AWS Lambda functions if the project includes .NET Core 1.1 dependencies.
-   Fixed issue with AWS CodeCommit integration on systems where the Team Explorer registry keys were not available or accessible.

## 1.11.7.1 (2017-04-19)

-   Fixed crash when encountering multiple copies of the same repository when refreshing repositories list in Team Explorer.

## 1.11.7.0 (2017-04-19)

-   Added support for cloning and creating AWS CodeCommit repositories in Team Explorer.
-   Added new 'Getting Started' page shown on first run of Visual Studio to set up AWS credentials, if none are found at startup by the toolkit.
-   Added support to the Register Account dialog in the AWS Explorer for importing AWS credentials from a CSV file that has been downloaded from the AWS Console.
-   Fixed issue with not listing all functions in the S3 dialog to invoke an AWS Lambda.

## 1.11.6.3 (2017-03-29)

-   Added support for deploying Node.js projects to AWS Lambda using the new Node.js v6.10 runtime.
-   Added support for using AWS Lambda in the Asia Pacific (Mumbai) region.

## 1.11.6.2 (2017-03-16)

-   Fixed issue with unused and irrelevant template to an 'AWS hosted control' appearing in File->New Item.

## 1.11.6.1 (2017-03-10)

-   Fixed issue causing package load failure on systems where the shared credential folder (%userprofile%\.aws) did not exist at startup.

## 1.11.6.0 (2017-03-13)

-   Added support for reading credentials from the shared credential file (%userprofile%\.aws\credentials) in addition to the existing sdk credential store.

## 1.11.5.0 (2017-03-10)

-   Added support for DynamoDB Time-to-Live.
-   Fixed issue with publishing Lambda functions and attempting to choose an IAM role.

## 1.11.4.0 (2017-02-20)

-   Improved Lambda deployment of platform specific dependencies.

## 1.11.3.0 (2017-02-09)

-   Improved Visual Studio theme support.
-   Added an alert when failing to list IAM roles for Lambda deployment due to missing permissions.
-   Added ability to specify cloudformation-role in aws-lambda-tools-defaults.json file an IAM role for CloudFormation to assume when creating or updating a stack.

## 1.11.2.0 (2017-01-05)

-   Added ability in AWS Lambda deployment wizard to save the deployment settings made in the wizard to aws-lambda-tools-defaults.json.

## 1.11.1.4 (2016-12-15)

-   Revised installer to resolve installation issues experienced by some users since the release of the .NET AWS Lambda support.
-   Fixed issue with illegal path characters when probing for dotnet.exe on some systems.

## 1.11.1.3 (2016-12-12)

-   Test release to verify installer changes.

## 1.11.1.2 (2016-12-10)

-   Fixed issue with deploying AWS Serverless Applications with named IAM resources.

## 1.11.1.1 (2016-12-08)

-   Update to latest version of the AWS SDK for .NET.

## 1.11.1.0 (2016-12-07)

-   New AWS Lambda projects will now create a global.json file to fix issues with users who also have Visual Studio 2017 RC installed.
-   Fix issue when creating an AWS Lambda project with tests where the src project was created twice.
-   Added the ability to select the PowerUserAccess managed policy when creating an IAM role.

## 1.11.0.0 (2016-12-01)

-   Added new .NET Core AWS Lambda Functions and AWS Serverless Application project types under the Visual C# section in the Visual Studio 2015 New Project wizard.
-   Added the ability to deploy AWS Lambda Functions and AWS Serverless Applications in Visual Studio 2015. Right click on the project to access the Publish to AWS Lambda wizard.
-   Added the ability to test invoke AWS Lambda Functions for the function view in the AWS Explorer.
-   Added the ability to configure Scheduled Events on AWS Lambda Functions from the event source tab in the AWS Lambda function view.
-   Added support for editing S3 Object Tags on the Object Properties dialog.
-   Fix issue with deploying CloudFormation templates with optional parameters.
-   Deprecated support for Visual Studio 2010 and 2012 editions. A separate installer can be downloaded for these versions at https://aws.amazon.com/visualstudio/.

## 1.10.0.6 (2016-10-19)

-   Fix issue causing local toolkit settings getting corrupted.

## 1.10.0.5 (2016-10-17)

-   Fix issues with CloudFormation editor parse errors.
-   Add AWS Explorer support for the new US East (Ohio) region.

## 1.10.0.4 (2016-10-10)

-   Fix issue with Fn::If function in the CloudFormation Editor.
-   Fix issue with not correctly identifing a resource type in the CloudFormation Editor.

## 1.10.0.3 (2016-08-31)

-   Fix issue with AWS Lambda (Node.js) project wizard now showing existing Node.js 4.3 functions.

## 1.10.0.2 (2016-08-24)

-   Fix issue with installer when Visual Studio is not installed.

## 1.10.0.1 (2016-08-23)

-   Fix issue with installed deployment manifest schema affecting users that manually author their deployment manifest.

## 1.10.0.0 (2016-08-23)

-   Added support for deploying ASP.NET Core applications to AWS Elastic Beanstalk.

## 1.9.6.22 (2016-07-12)

-   Fix issue with creating a keypair during deployment.
-   Fix issue with creating an IAM role during deployment.

## 1.9.6.21 (2016-06-09)

-   In Node.js Lambda plugin allow setting runtime to version 4.3 and timeouts greater then one minute.

## 1.9.6.20 (2016-05-19)

-   Fix issue with editing DynamoDB table indexes in the Table Properties dialog; users were not able to add a new entry and then delete it without committing the change.

## 1.9.6.19 (2016-03-10)

-   Added support for opening remote desktop connections to Amazon EC2 instances running in VPCs using their private IP addresses, for instances that do not have Elastic IP addresses assigned.

## 1.9.6.18 (2016-03-08)

-   Renamed the AWS project template hierarchy beneath the Visual C# new project tree to 'AWS Sample Projects', to distinguish from the higher level 'AWS' category containing the AWS CloudFormation and AWS Lambda project types.

## 1.9.6.17 (2016-02-29)

-   Fix issue with standalone deployment tool, awsdeploy.exe, not handling credentials contained in deployment configuration file correctly resulting in the message 'No account found for the given parameters'.

## 1.9.6.16 (2016-02-17)

-   Fix issue with dark theme detection and some hard-to-read windows and views for IAM.

## 1.9.6.15 (2016-02-11)

-   Fix issue with invalid credential profiles causing the toolkit to crash on startup.

## 1.9.6.14 (2016-02-07)

-   Fix issue with creating zip archive for Node.js Lambda functions.

## 1.9.6.13 (2016-02-03)

-   Fix issue with locating msdeploy.exe during website deployments for Windows 10 systems upgraded from prior versions.

## 1.9.6.12 (2016-01-29)

-   This version was used for internal testing and not released publicly.

## 1.9.6.11 (2015-12-07)

-   Fix issue with CloudFormation editor saving template files with a byte order mark that CloudFormation web console couldn't handle.
-   Fix issues with using the CloudFormation Editor and Elastic Beanstalk deployment wizard in the China region.

## 1.9.6.10 (2015-12-01)

-   Fixes for SDK credentials store to contain SAML based profiles.

## 1.9.6.9 (2015-11-23)

-   Fix issue with RDS instance identifier validation.

## 1.9.6.8 (2015-11-13)

-   Updated Elastic Beanstalk deployment wizard to select the IIS App pool's .NET Runtime instead of .NET Framework.

## 1.9.6.7 (2015-10-22)

-   Fix issues in Lambda function view for managing event sources.

## 1.9.6.6 (2015-10-14)

-   Fix issue with handling corrupted credentials profile.

## 1.9.6.5 (2015-09-28)

-   Fix issue accessing last used settings in deployment wizard.

## 1.9.6.4 (2015-08-24)

-   Fix issue in CloudFormation editor with special AWS parameter types like AWS::EC2::Image::Id.

## 1.9.6.3 (2015-08-18)

-   Fix additional issues with the AWS CloudFormation deployment wizard showing black field labels in dark theme.

## 1.9.6.2 (2015-08-17)

-   Fix issue with various windows not correctly handling the dark theme in Visual Studio 2015.

## 1.9.6.1 (2015-07-31)

-   Fix issue with displaying table and stream property dialog boxes from Amazon DynamoDB Tables.

## 1.9.6.0 (2015-07-28)

-   Fix security issue with storing proxy credentials unencrypted in the user's private toolkit settings file.
-   Update to use the new version 3 AWS SDK for .NET.
-   Added ability to enable Amazon DynamoDB Streams.
-   Added ability to add Amazon DynamoDB Streams as event sources for AWS Lambda functions.

## 1.9.5.2 (2015-07-14)

-   Fixed issue with invalid enum when creating https-only Amazon CloudFront distribution.

## 1.9.5.1 (2015-07-07)

-   Revised display of Amazon EC2 instance type dropdowns, removing type 'name' in favor of just type code, grouped by hardware family.

## 1.9.5.0 (2015-06-24)

-   Fixed issue with 'security group not found' errors when deploying to Elastic Beanstalk and the option to update Amazon RDS security groups was selected.
-   Updated EC2 Launch Wizard to vary the default volume size based on the selected image.

## 1.9.4.0 (2015-05-28)

-   Updated VPC support in EC2 Launch Wizard, Deployment Wizard and RDS Wizard.
-   New DB subnet group view for RDS.
-   Instance types in EC2 drop down boxes are now categorized by hardware family.

## 1.9.3.1 (2015-05-26)

-   Fix issue with DynamoDB browser when using the Between operator.

## 1.9.3.0 (2015-05-06)

-   Update Lambda features to use new permission model.
-   Added support for subscribing Lambda functions to a SNS topic.
-   Added support for deleting log streams from Lambda function view.
-   Fix issue with uploading new versions of Lambda functions.
-   Fix issue with adding new profiles in the Publish To AWS deployment wizard.
-   Fix issue with setting IIS app path.
-   Fix issues with referencing parameters in CloudFormation editor.

## 1.9.2.2 (2015-04-16)

-   Fix issue with CloudFormation stack name validation.

## 1.9.2.1 (2015-04-09)

-   Fix issue with detecting double-click on short object keys in Amazon S3 bucket browser view.
-   Fix issue with starting New AWS Lambda project wizard.

## 1.9.2.0 (2015-03-27)

-   Added support for Visual Studio 2015 Preview.

## 1.9.1.2 (2015-03-24)

-   Fix issue with double-click on scrollbar thumb in Amazon S3 bucket browser view.
-   Fix issue with adding CloudFormation template to a CloudFormation project.

## 1.9.1.1 (2015-03-18)

-   Fix issue with viewing CloudWatch Logs for Lambda function.

## 1.9.1.0 (2015-03-12)

-   Updated AWS Lambda support to be able to view CloudWatch Logs from function view.
-   Fixed issue with C# project templates not showing up correctly.

## 1.9.0.0 (2015-03-05)

-   Added support for testing and deploying AWS Lambda functions. This requires that the Node.js Tools are installed. For more information: https://blogs.aws.amazon.com/net/post/Tx381XNNQALP8BA/
-   Added support to Amazon S3 bucket properties to configure event notifications.

## 1.8.2.1 (2015-02-10)

-   Fix minor window layout issue

## 1.8.2.0 (2015-02-10)

-   Added support for setting version label in the new Publish To AWS deployment wizard.
-   Added support for solution platform in addition to solution build configuration when building projects for deployment.

## 1.8.1.0 (2015-01-27)

-   Added support for updating global secondary indexes on an existing Amazon DynamoDB table.

## 1.8.0.3 (2015-01-15)

-   Fixed issue with 'E_INVALIDARG' build errors during deployment when custom solution build configuration names are used that do not correspond to project build configuration names.

## 1.8.0.2 (2015-01-08)

-   Fixed issue with custom health check behavior in the new deployment wizard.
-   Fixed issue with not persisting last-used build configuration in the new deployment wizard.

## 1.8.0.1 (2014-12-30)

-   Internal-only test release.

## 1.8.0.0 (2014-12-17)

-   Updated the deployment wizard experience for AWS Elastic Beanstalk.
-   Added support for new AWS CloudFormation parameter types in the CloudFormation editor.
-   Added the ability to purge an Amazon Simple Queue Service queue.
-   Added the ability to easily delete AWS Identity and Access Management users, groups and roles including all dependencies.

## 1.7.1.1 (2014-11-13)

-   Fixed issue with Amazon S3 properties window for SSE-C objects.

## 1.7.1.0 (2014-11-12)

-   Added support to recognize AWS Key Management Service encryption support with Amazon S3 objects.

## 1.7.0.0 (2014-11-06)

-   Added support for Visual Studio themes.
-   Added support for using SSD volumes types in the Amazon EC2 launch wizard.

## 1.6.9.0 (2014-10-23)

-   Added support for EU Central (Frankfurt) region.

## 1.6.8.0 (2014-10-08)

-   Made the Amazon DynamoDB table browser compatible with the new Amazon DynamoDB data types.
-   Fix JSON parsing bug in the AWS CloudFormation editor.

## 1.6.7.1 (2014-07-24)

-   Fix issue with starting DynamoDB Local when Java is not installed.

## 1.6.6.3 (2014-06-20)

-   Add support in RDS DB Instance view for creating Multi AZ SQL Server databases.

## 1.6.6.2 (2014-06-04)

-   Bug fixes in the Amazon DynamoDB Table Properties dialog.

## 1.6.6.1 (2014-05-22)

-   Bug fixes in the AWS Elastic Beanstalk Environment view.

## 1.6.6.0 (2014-05-14)

-   Fixed a conflict issue with the AWS CloudFormation editor and Visual Studio 2013 Update 2's JSON editor.

## 1.6.5.4 (2014-04-03)

-   Fixed an issue with Account Type dropdown in the Add Account dialog where it displayed blank values.

## 1.6.5.3 (2014-03-20)

-   Fix timeout issue when uploading large applications for Elastic Beanstalk deployments.

## 1.6.5.2 (2014-03-07)

-   Fix for CloudWatch metrics for AWS CloudFormation deployment views.
-   Fix for updating security groups when connecting via SSH to Linux instances.

## 1.6.5.1 (2014-03-06)

-   Fixed the display of AWS CloudWatch metrics for AWS Elastic Beanstalk deployments.

## 1.6.5.0 (2014-02-21)

-   Add support for dead letter queue for Amazon SQS.
-   Performance improvements in JSON parsing for CloudFormation Editor.
-   Fix issue with installing DynamoDB Local.

## 1.6.4.0 (2014-01-29)

-   Improved support of Visual Studio's Dark Theme with the CloudFormation Editor.
-   CloudFormation templates used to create stacks from the AWS Explorer our uploaded to Amazon S3 to enable larger templates to be used for stack creation.

## 1.6.3.0 (2014-01-16)

-   Integrated Amazon DynamoDB Local into AWS Explorer for local testing.
-   Add support for Global Secondary Indexes into the Amazon DynamoDB Create Table Wizard.

## 1.6.2.0 (2013-12-19)

-   Add support for Resource Conditions in the AWS CloudFormation Editor.

## 1.6.1.1 (2013-12-13)

-   Fix issue with using conditions in AWS CloudFormation templates.

## 1.6.1.0 (2013-12-11)

-   Add resource condition support to the AWS CloudFormation editor
-   Add Amazon Simple Workflow image processing sample

## 1.6.0.2 (2013-11-21)

-   Fixed issue in SDK that blocked some CloudFormation deployments.

## 1.6.0.1 (2013-11-11)

-   Fixed issue with remote desktop capability not being available for Windows instances.

## 1.6.0.0 (2013-11-08)

-   Moved to version 2 of the AWS SDK for .NET

## 1.5.6.2 (2013-10-17)

-   Adjust default write capacity for new Amazon DynamoDB tables

## 1.5.6.1 (2013-10-09)

-   Add the ability to specify the provision iops when creating a volume.
-   Add the ability to highlight and copy the value of key fields in the Amazon DynamoDB table browser.

## 1.5.6.0 (2013-09-20)

-   Fix issue with AWS CloudFormation deployment for large template files.

## 1.5.5.0 (2013-08-21)

-   Added support for installation into Visual Studio 2013 Preview.

## 1.5.4.0 (2013-08-13)

-   Added support to make the domain name field on Amazon CloudFront distribution views function as a clickable link.

## 1.5.3.1 (2013-07-19)

-   Fix issue preventing deletion of disabled Amazon CloudFront distributions from the AWS Explorer.
-   Fix issue that could cause Visual Studio to occasionally crash when changing the type of AWS Elastic Beanstalk environments.
-   Fix issue with deployment from Visual Studio using AWS Identity and Access Management user accounts that caused a new Amazon S3 bucket to be created for each IAM account.

## 1.5.3.0 (2013-07-17)

-   Added support for deployment to the new AWS Elastic Beanstalk 'Single-instance' environment type.

## 1.5.2.3 (2013-07-10)

-   Fix issue with not being able to redeploy to AWS CloudFormation stacks in 'rollback complete' state.

## 1.5.2.2 (2013-06-19)

-   Fix issue subnet view showing an incorrect route table for the subnet.
-   In the route table view add the ability to change the main route table for a VPC.

## 1.5.2.1 (2013-05-16)

-   Fix issue with update stack wizard showing only the first 10 stacks.
-   Fix issue with loading the AWS DynamoDB editor

## 1.5.2.0 (2013-05-15)

-   Added support for showing secondary indexes in Amazon DynamoDB table views
-   Fix issue with AWS Explorer showing a maximum of 100 tables for Amazon DynamoDB
-   Fix issue with selecting security groups appropriate for VPC-only accounts
-   Fix issue with selecting non-default IAM role during deployment to AWS Elastic Beanstalk

## 1.5.1.1 (2013-05-07)

-   Add support for DynamoDB Local Secondary Indexes (LSI) in the AWS Explorer.

## 1.5.1.0 (2013-04-17)

-   Add support for specifying an AWS Identity and Access Management role when deploying to AWS Elastic Beanstalk.

## 1.5.0.2 (2013-04-09)

-   Fix an installer issue when upgrading from a previous version of the Toolkit.

## 1.5.0.1 (2013-04-09)

-   Fix an installer issue when upgrading from a previous version of the Toolkit.

## 1.5.0.0 (2013-04-08)

-   Elastic Beanstalk for .NET now supports configuration files and launching inside a VPC.
-   Add Amazon VPC support including Subnets, Elastic IPs, Route Tables, Security Groups, Internet Gateways and Network Acls.
-   New project templates demonstrating many common use cases for the AWS SDK for .NET.

## 1.4.0.4 (2013-03-11)

-   Add support to copy AMI between regions.
-   Add the ability to empty a S3 bucket before deleting the bucket.

## 1.4.0.3 (2013-02-27)

-   Add the Cancel Update action in the AWS CloudFormation stack view.

## 1.4.0.2 (2013-02-14)

-   Enhancements to EC2 instance launch wizard.

## 1.4.0.1 (2013-01-23)

-   Add Stack ID to the AWS CloudFormation Stack view.
-   Fix issue with Connect button in AWS CloudFormation Stack view.

## 1.4.0.0 (2012-12-21)

-   Add a new project type called "AWS CloudFormation Project" which can be used for authoring, validating and deploying AWS CloudFormation templates.

## 1.3.6.0 (2012-11-19)

-   Add support for deploying to Windows Server 2012/IIS 8 with AWS CloudFormation and AWS Elastic Beanstalk.
-   Fix issue with deployment of website projects including additional folders outside of the website project folder.

## 1.3.5.0 (2012-11-13)

-   Add ability to view logs in AWS Elastic Beanstalk environment view.
-   Add ability to generate a deployment configuration file from an AWS Elastic Beanstalk environment in the AWS Explorer that can be used by awsdeploy.exe for command line deployments.
-   Updated S3 bucket properties to allow a lifecycle to be specified that transitions objects to Amazon Glacier.
-   Add new command in S3 browser to restore objects from Amazon Glacier whose current storage class is "GLACIER".
-   Add ability to right click a SQL Server instance in the RDS view and copy its address to the clipboard.
-   Fix issue with the RDS launch wizard not showing the correct parameter groups for the selected engine version.

## 1.3.4.1 (2012-11-02)

-   Fix paging issue AWS CloudFormation in the AWS Explorer.

## 1.3.4.0 (2012-10-05)

-   Add ability to set website redirect locations in the Amazon S3 object properties dialog.
-   Add ability to set price class for Amazon CloudFront distributions.

## 1.3.3.3 (2012-10-03)

-   Fix issue in wizard when publishing to a new AWS Elastic Beanstalk environment.

## 1.3.3.2 (2012-09-23)

-   Fix performance issue loading elements into AWS Explorer.
-   Add option to open DB Instance view after launching a new instance.

## 1.3.3.1 (2012-08-31)

-   Fix issues with deploying existing AWS Beanstalk application versions from the application view screen.

## 1.3.3.0 (2012-08-21)

-   Added support for Amazon DynamoDB binary types

## 1.3.2.1 (2012-07-11)

-   Fix issue with not detecting MSDeploy v3 RC install during deployments from machines that only have Visual Studio 2012 RC
-   Fix issue with deployment wizard resetting fields on AWS/Application Options pages when navigating back through the wizard
-   Fix issue when connecting to an instance for an environment failed if the AWS Explorer was set to a different region
-   Added support for using AWS Identity and Access Management when creating AWS CloudFormation stacks
-   Fix issue causing Amazon CloudFront invalidations to fail due to not always receiving a /-prefixed object key when invoked from the Amazon S3 Bucket Browser

## 1.3.2.0 (2012-06-26)

-   Added support for Visual Studio 2012 RC
-   Added support for setting application options in deployment wizard for both AWS CloudFormation and AWS Elastic Beanstalk deployments

## 1.3.1.0 (2012-06-11)

-   Fix issue with incremental deployment not detecting deleted/excluded files during push to Git.
-   Add support for AWS Identity and Access Management Instance Profiles (Roles) for launching an Amazon EC2 instance.
-   Add support for creating AWS Identity and Access Management Instance Profiles (Roles).
-   Add support for setting/updating application settings and credentials when deploying to AWS Elastic Beanstalk.
-   Improvements to the Amazon S3 bucket view for buckets containing large numbers of files.

## 1.3.0.7 (2012-05-29)

-   Update sample application for awsdeploy.exe.

## 1.3.0.6 (2012-05-24)

-   Fix issue uploading large web deploy archives for AWS Elastic Beanstalk deployments.

## 1.3.0.4 (2012-05-15)

-   Fix issue with version mismatch in 3rd party libraries leading to problems loading ICSharpCode.SharpZipLib.dll on some systems (public release).
-   Updates to maintain compatibility with Amazon CloudFront changes in .Net SDK 1.4.10 release.

## 1.3.0.3 (2012-05-15)

-   Fix issue with version mismatch in 3rd party libraries leading to problems loading ICSharpCode.SharpZipLib.dll on some systems (private forum release for testing).

## 1.3.0.2 (2012-05-14)

-   Fix issue with loading plugins on non en-us systems, leading to empty AWS Explorer window.

## 1.3.0.1 (2012-05-10)

-   Fix issue with getting an illegal character error during incremental deployment.

## 1.3.0.0 (2012-05-08)

-   Add web application deployment support for AWS Elastic Beanstalk plus 'fast' redeployment to existing AWS CloudFormation/AWS Elastic Beanstalk deployments.
-   Add support for Amazon RDS and Microsoft SQL Server.
-   Add support to standalone deployment tool for AWS Elastic Beanstalk. Also added AWS CloudFormation 'update stack' functionality.

## 1.2.4.7 (2012-04-26)

-   Add support in deployment wizard to retrieve and offer custom health check URL from deployed instances during redeployment.

## 1.2.4.6 (2012-04-24)

-   Fix issue in deployment wizard blocking n querying prior deployment when instances not responding.

## 1.2.4.5 (2012-04-23)

-   Fix upgrade-install issue with AWSDeploymentCryptoUtility.dll not being updated, causing redeployment issues.

## 1.2.4.4 (2012-04-22)

-   Fix issue deploying to non us-east-1 regions.

## 1.2.4.3 (2012-04-19)

-   Fix issue with non-responsive wizard when republishing to AWS CloudFormation.

## 1.2.4.2 (2012-04-16)

-   Fix issue with getting a load failure on the AWSDeploymentCryptoUtility.dll when publishing to AWS CloudFormation.

## 1.2.4.1 (2012-03-16)

-   Fix issue with getting a "Cannot access a disposed object" error.

## 1.2.4.0 (2012-03-13)

-   Fix issue where the AWS Explorer window fails to display content due to an issue in locating supporting assemblies.

## 1.2.3.0 (2012-03-09)

-   Add support for the new Amazon EC2 m1.medium instance type and the addition of 64bit support in the existing m1.small and c1.medium instance types.
-   Add support for creating alarms when creating Amazon DynamoDB tables.

## 1.2.2.0 (2012-02-21)

-   Fix issue with drag and drop of Amazon DynamoDB table ARNs.

## 1.2.1.0 (2012-02-02)

-   Add support for Object Expiration in the Amazon S3 bucket properties.
-   Change Amazon DynamoDB editor to limit results to 100 rows per page if no scan condition is set.

## 1.2.0.0 (2012-01-18)

-   Add support for Amazon DynamoDB a fast, highly scalable, highly available, cost-effective, non-relational database service.
-   Add support for SMS messaging with Amazon SNS in the US East region.

## 1.1.2.0 (2011-11-09)

-   Updated Amazon S3 browser to use multi object delete when deleting objects.

## 1.1.1.0 (2011-11-09)

-   Fix issue with connecting to EC2 instances with multiple security groups.
-   Fix issue with attempting to creating buckets with invalid names for regions outside of US East.

## 1.1.0.0 (2011-10-21)

-   New command line tool that enables you to deploy your application to AWS CloudFormation from outside of the Microsoft Visual Studio environment.
-   Customize Columns in AMI, Instance, and Volume Views.
-   Tagging of AMIs, Instances, and Volumes.
-   Access to GovCloud for AWS accounts designate as GovCloud users.
-   Pagination of result set returned by Amazon SimpleDB.
-   Export Amazon SimpleDB Results to CSV.
-   Set Server-Side Encryption in Amazon S3.
-   Time Delayed Message Delivery in SQS.

## 1.0.0.0 (2011-09-08)
