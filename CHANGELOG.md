## 1.84.0.0 (2026-01-08)

- **Feature** Copy next steps file to source folder on apply changes, enabling it to be bundled in subsequent AWS Transform jobs

## 1.83.0.0 (2025-12-17)

- **Feature** Add support for deploying .NET 10 AWS Lambda Functions
- **Feature** Visual Studio 2026 support is now generally available.

## 1.82.0.0 (2025-12-01)

- **Feature** Adding agentic AWS Transform for .NET and separating login experience for Amazon Q and AWS Transform, enabling customers to use both features sets in same session

## 1.81.0.0 (2025-11-13)

- **Bug Fix** Fix issue getting an incompatible version of private packages for AWS Transform for .NET
- **Bug Fix** Update warning about build failure before starting AWS transform job
- **Feature** Optimized AWS Transform to upload only selected project and its dependencies
- **Feature** Allow projects already targeting the destination framework version and projects with build errors to be processed by AWS Transform

## 1.80.0.0 (2025-11-06)

- **Breaking Change** AWS CodeCommit support has been removed from Visual Studio 2026. CodeCommit features remain available in Visual Studio 2022. For more information about CodeCommit, see https://docs.aws.amazon.com/codecommit/
- **Feature**  Preview support for Visual Studio 2026 has been added. Please report any issues encountered on GitHub: https://github.com/aws/aws-toolkit-visual-studio/issues/new/choose

## 1.79.1.0 (2025-10-30)

- **Bug Fix** Improved error messaging when transformation fails due to duplicate project.

## 1.79.0.0 (2025-10-13)

- **Breaking Change** Publish to AWS has been updated to use v2.0.4 of the AWS .NET deploy tool. This version of the Toolkit includes the following Deploy Tool changes:
  - Upgrade the Deploy Tool from .NET 6 to .NET 8.
  - Update AWS .NET SDK to V4.
 - See https://github.com/aws/aws-dotnet-deploy/releases/tag/release_2025-05-01, https://github.com/aws/aws-dotnet-deploy/releases/tag/release_2025-06-05, https://github.com/aws/aws-dotnet-deploy/releases/tag/release_2025-06-16, https://github.com/aws/aws-dotnet-deploy/releases/tag/release_2025-06-25, https://github.com/aws/aws-dotnet-deploy/releases/tag/release_2025-07-15, https://github.com/aws/aws-dotnet-deploy/releases/tag/release_2025-09-08 and https://github.com/aws/aws-dotnet-deploy/releases/tag/release_2025-09-24 for more details.
- **Breaking Change** The extension has been updated to use AWS SDK for .NET V4.0. Some functionality may be impacted as a result of this migration, please report any issues encountered with this version on GitHub: https://github.com/aws/aws-toolkit-visual-studio/issues/new/choose

## 1.78.0.0 (2025-09-11)

- **Feature** Rename button in Transformation summary view from Download Summary to Download Transformation Report

## 1.77.3.0 (2025-09-04)

- **Bug Fix** Transformation Job History menu now available when in-progress transformation exist for the current solution.
- **Bug Fix** Fix private package index error and issue loading nuget sources with creds for .NET transformations

## 1.77.2.0 (2025-08-28)

- **Bug Fix** Simplified dashboard layout by removing readiness columns in transformation plan.
- **Bug Fix** Introducing cache validation to eliminate stale data causing transformation failures.

## 1.77.1.0 (2025-08-21)

- **Bug** Remove popup dialog with AWS Transform when porting unsupported project type

## 1.77.0.0 (2025-08-13)

- **Bug Fix** Improvements to Transformation Job State Management.
- **Feature** Added dynamic model selection support across all regions.

## 1.76.0.0 (2025-08-06)

- **Feature** Added profile-aware transformation job management
- **Feature** Added Focused Logging for developer Profile

## 1.75.0.0 (2025-07-16)

- **Feature** Image support has been added to agentic chat

## 1.74.0.0 (2025-07-02)

- **Bug Fix** Pressing Home or End in the chat panel no longer switches focus to another ToolWindow
- **Feature** Adding abap content type to enable inline completions
- **Feature** Pinned context support has been added to agentic chat

## 1.73.0.0 (2025-06-18)

- **Feature** MCP support has been added to agentic chat
- **Feature** Model selection has now been added in Agentic Chat

## 1.72.0.0 (2025-06-11)

- **Feature** Add call to action in chat to subscribe to Q Developer Pro if monthly request limit is reached

## 1.71.0.0 (2025-06-05)

- **Feature** Agentic chat is now available - use natural langauge prompts in Q Chat to read, create, and alter files, generate code diffs, run command-line tasks, and much more.
- **Feature** Add support for project rules, which are added as context in all of your Q chat interactions - https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/context-project-rules.html
- **Feature** AWS Transform now downloads an html version of the transform summary in addition to the markdown version.

## 1.70.0.0 (2025-05-15)

- **Feature** Add Transformation History feature
- **Feature** Enable Private Nuget Support with Transformation
- **Feature** Add Transformation Summary feature
- **Feature** Enable ASP.NET Razor Views porting 
- **Feature** Add separate auth workflow for AWS Transform

## 1.69.0.0 (2025-05-08)

- **Feature** Publish to AWS has been updated to use v1.29.0 of the AWS .NET deploy tool. This version of the Toolkit includes the following Deploy Tool changes:
  - Add support for deploying ARM web apps to ECS Fargate
  - Add support for deploying ARM console apps to ECS Fargate
  - Add support for deploying ARM web apps to Elastic Beanstalk on Linux
  - See https://github.com/aws/aws-dotnet-deploy/releases/tag/release_2025-04-24 for more details.

## 1.68.0.0 (2025-04-09)

- **Feature** Add support for choosing and switching between Amazon Q Developer profiles.
- **Feature** Add Tooltip to Amazon Q icon in the document margin. The Tooltip presents Amazon Q connection details and error messages.

## 1.67.0.0 (2025-04-03)

- **Bug Fix** The IAM Identity Center configuration view will now accept Start Urls that end with a slash

## 1.66.0.0 (2025-03-13)

- **Bug Fix** Fix Method not found error with NuGet and FindPackageByIdResource when loading Publish to AWS.
- **Feature** Amazon Q Developer .NET Transform job histories for the current solution can now be viewed from the 'Extensions > AWS Toolkit > Amazon Q Developer > Transformation Job History' menu

## 1.65.0.0 (2025-02-03)

- **Bug Fix** Fixed a compatibility issue that caused problems with C/C++ functionality in other extensions like Visual Assist.
- **Bug Fix** Add support for SSL validation. If you are using your IDE on a network that uses custom SSL certificates, you can configure the extension with your PEM based certificate. Tools > Options > AWS Toolkit > Proxy > Certificate Authority.
- **Bug Fix** Improve proxy support preventing Q features from working in certain networking configurations.

## 1.64.0.0 (2025-01-15)

- **Feature** The Q Chat generative AI disclaimer is now dismissable. Once acknowledged, the state is stored in Tools > Options > AWS Toolkit > Amazon Q under Q Chat.

## 1.63.0.0 (2024-12-18)

- **Feature** Publish to AWS has been updated to use v1.28.0 of the AWS .NET deploy tool. This version of the Toolkit includes the following Deploy Tool changes:
  - Update beanstalk platform resolution logic to additionally use 'Deprecated' versions in order to continue supporting .NET 6.
  - See https://github.com/aws/aws-dotnet-deploy/releases/tag/release_2024-11-15 for more details.

## 1.62.0.0 (2024-12-16)

- **Bug Fix** The confirmation dialog now shows the full url when clicking a link from Q Chat
- **Feature** Added support for additional languages in Amazon Q. This version of the Toolkit introduces support for the following languages: JSON, SQL, PowerShell, and Bash scripts.

## 1.61.0.0 (2024-12-03)

- **Feature** Add support for "Amazon Q Developer transform for .NET". You can now port your .NET Framework applications to cross-platform .NET.

## 1.60.0.1 (2024-11-15)

- **Bug Fix** Fix Amazon Q features not working in Visual Studio v17.12 - https://github.com/aws/aws-toolkit-visual-studio/issues/478

## 1.60.0.0 (2024-11-08)

- **Bug Fix** Fixed issue where SSO prompt could appear when disabling the Amazon Q feature in the Getting Started experience.
- **Feature** Publish to AWS has been updated to use v1.27.0 of the AWS .NET deploy tool. This version of the Toolkit includes the following Deploy Tool changes:
  - Added support for .NET 9 in deployment recipes.
  - Added ability to configure EC2 IMDSv1 access for the Windows and Linux Elastic Beanstalk recipes.
  - Support Elastic Beanstalk's transition to using EC2 Launch Templates from the deprecated Launch Configuration. This is required for AWS accounts created after October 1st 2024.
- **Feature** Pull in latest changes of Amazon.ECS.Tools for ECS deployment:
  - Fixed values for task-definition-volumes and container-mount-points properties not correctly being parsed.
- **Feature** Pull in latest changes of Amazon.ElasticBeanstalk.Tools for Elastic deployment:
  - Added ability to disable IMDS v1 by setting the disable-imds-v1 property in the aws-beanstalk-tools-defaults.json.
- **Feature** Pull in latest changes of Amazon.Lambda.Tools for Lambda deployment:
  - Add the log-format, log-application-level, log-system-level and log-group properties that can be set in the aws-lambda-tools-defaults.json file.
  - Fixed an issue where CodeUri set in Globals section is ignored for AWS::Serverless::Function resource.
  - Update the dependencies for the embedded zipping utility used to set file permissions correctly when creating deployment bundles on Windows.
  - Fixed issue with the configured architecture of the Lambda function not being used when building the container image. This caused images to be built for X64 when the function was configured for ARM64.

## 1.59.0.0 (2024-10-24)

- **Bug Fix** Fix a bug that could cause the IDE to freeze during startup
- **Feature** The extension's Getting Started experience has been improved:
  - Added ability to enable and disable AWS Toolkit and Amazon Q feature sets. This allows control over which parts of the extension are integrated with Visual Studio.
  - The Getting Started experience is automatically displayed the first time Visual Studio is launched after installing this version (or a newer version).
  - Added option to access the Getting Started experience at any time from the "Extensions" > "AWS Toolkit" > "Getting Started" menus.
- **Feature** Publish to AWS has been updated to use v1.26.1 of the AWS .NET deploy tool. This version of the Toolkit includes the following Deploy Tool changes:
  - Fixed container deployment failures on Apple silicon by ensuring X64 platform specification.
  - Addressed deployment failures caused by System.Text.Json issues by pinning the version to mitigate .NET 9 bugs.
  - See https://github.com/aws/aws-dotnet-deploy/releases/tag/1.25.3, https://github.com/aws/aws-dotnet-deploy/releases/tag/release_2024-09-27 and https://github.com/aws/aws-dotnet-deploy/releases/tag/release_2024-10-11 for more details.

## 1.58.1.0 (2024-09-19)

- **Bug Fix** Performance improvements when automatically generating inline code suggestions with Amazon Q.
- **Bug Fix** Troubleshooting instructions to fix extension start-up issues reported since version 1.54.0.0 (https://github.com/aws/aws-toolkit-visual-studio/issues/452) is now listed in the output window. An info bar has been added to the toolkit as a reminder: see [guide](https://docs.aws.amazon.com/toolkit-for-visual-studio/latest/user-guide/general-troubleshoot.html#general-troubleshoot-component-initilization) for details.

## 1.58.0.0 (2024-09-05)

- **Feature** Publish to AWS has been updated to use v1.24.4 of the AWS .NET deploy tool. This version of the Toolkit includes the following Deploy Tool changes:
  - Projects can now be deployed to Elastic Beanstalk without requiring self-contained builds.
  - Fix deployment failure when System.Text.Json detects a dependency that has a listed vulnerability.
  - See https://github.com/aws/aws-dotnet-deploy/releases/tag/1.23.4 and https://github.com/aws/aws-dotnet-deploy/releases/tag/1.24.4 for more details.

## 1.57.0.0 (2024-08-22)

- **Bug Fix** Amazon Q Chat now uses the currently active code document as context. This makes it easier to ask questions about your code without needing to add it to your prompt.
- **Feature** When Amazon Q is running a security scan, a progress indicator is now shown next to the Q icon in the margin.

## 1.56.0.0 (2024-08-01)

- **Feature** Publish to AWS has been updated to use v1.22.5 of the AWS .NET deploy tool. This version of the Toolkit includes the following Deploy Tool changes:
  - Performance improvements when editing deployment configurations.
  - When configuring a deployment to an existing target, fewer fields will be shown when they cannot be adjusted.
  - Add support for choosing between a "Public" and an "Internal" Load Balancer when deploying an Elastic Beanstalk application into a VPC
  - See https://github.com/aws/aws-dotnet-deploy/releases/tag/1.20.8, https://github.com/aws/aws-dotnet-deploy/releases/tag/1.21.13, and https://github.com/aws/aws-dotnet-deploy/releases/tag/1.22.5 for more details.
- **Feature** When Amazon Q is generating an inline suggestion, a progress indicator is now shown next to the Q icon in the margin.

## 1.55.2.0 (2024-07-22)

- **Bug Fix** Fix "Unable to find an entry point named '?' in DLL 'WebView2Loader.dll" error when attempting to view Amazon Q Chat.
- **Bug Fix** Performance improvements in the Publish to AWS deployment configuration screens

## 1.55.1.0 (2024-07-16)

- **Bug Fix** Added more safeguards to extension start-up based on issues reported in version 1.54.0.0 (https://github.com/aws/aws-toolkit-visual-studio/issues/441)

## 1.55.0.0 (2024-07-11)

- **Bug Fix** Fix issue where settings could be overwritten when navigating between different settings pages
- **Deprecation** This is the last planned AWS Toolkit release for Visual Studio 2019. You are encouraged to run Visual Studio 2022, and the corresponding AWS Toolkit extension. An info bar has been added to the Toolkit as a reminder - see https://github.com/aws/aws-toolkit-visual-studio/issues/447 for details.

## 1.54.0.1 (2024-07-03)

- **Bug Fix** Added safeguards to extension start-up based on issues reported in version 1.54.0.0 (https://github.com/aws/aws-toolkit-visual-studio/issues/441)

## 1.54.0.0 (2024-07-02)

- **Feature** Amazon Q is now generally available for Visual Studio 2022. Use Amazon Q Chat to help author, explain, refactor, fix, and optimize code. Run security scans on C# code to catch security vulnerabilities.

## 1.53.0.0 (2024-05-23)

- **Feature** The AWS Builder Id and IAM Identity Center (SSO) login flow has been improved to support authorization code + PKCE in supported regions.  This new flow simplifies the login process by eliminating the need to verify a code while remaining secure.  The device code flow will continue to be used in regions that do not support the authorization code + PKCE flow.

## 1.52.0.0 (2024-05-09)

- **Bug Fix** Fix issue where Amazon Q inline suggestions would appear over-indented

## 1.51.0.0 (2024-04-29)

- **Feature** Amazon CodeWhisperer functionality is now part of Amazon Q Developer. All existing CodeWhisperer features will continue to function including inline code suggestions.

## 1.50.0.0 (2024-03-28)

- **Bug Fix** Fix issue where IAM IdC sign-ins for non-US sign-in portals would not automatically refresh when using CodeWhisperer
- **Deprecation** Removed the nodejs12.x runtime from Lambda deployment dialogs. This runtime has reached end of support. See https://docs.aws.amazon.com/lambda/latest/dg/runtime-support-policy.html for more details.
- **Feature** Publish to AWS has been updated to use v1.19.13 of the AWS .NET deploy tool. This version of the Toolkit includes the following Deploy Tool changes:
  - Security group settings now show the group name in addition to the group id
  - Fix deprecated Lambda runtime failure when deploying Blazor projects
  - Blazor WebAssembly deployments now allow CloudFront to write to the access log S3 bucket
  - See https://github.com/aws/aws-dotnet-deploy/releases/tag/1.19.13 for more details.
- **Removal** Removed Node.js related AWS Lambda Project Templates

## 1.49.0.0 (2024-03-07)

- **Bug Fix** Fixed issue with not building Lambda container image for ARM when function architecture is configured for ARM
- **Feature** Publish to AWS has been updated to use v1.18.6 of the AWS .NET deploy tool. Projects can now be deployed to Elastic Beanstalk on Linux using the '.NET 6 on AL2023' platform. See https://github.com/aws/aws-dotnet-deploy/releases/tag/1.18.6 for more details.

## 1.48.0.0 (2024-02-22)

- **Feature** Added support for using container builds with Lambda when targeting .NET 8
- **Feature**  Add support for publishing Lambda functions using the .NET 8 managed runtime

## 1.47.0.0 (2024-02-08)

- **Bug Fix** Fix "Bucket is not in the same region" validation in Serverless deployment dialog when working with buckets in eu-west-1.
- **Feature** Publish to Beanstalk experience now defaults to using self contained deployment bundles when publishing .NET 8 projects to Linux images. This setting is necessary for Beanstalk Linux images that do not support .NET 8.
- **Feature** Added local debugging support for .NET 8 Lambda projects using the Lambda Test Tool.
- **Feature** The AWS Builder Id and IAM Identity Center (SSO) login flow has been improved to confirm that the device code in the Toolkit and browser match. Previously, the code needed to be copied from the Toolkit and pasted into the browser.
- **Feature** CodeWhisperer functionality can be fully enabled and disabled from the AWS Toolkit / CodeWhisperer section of the Visual Studio Options dialog.
- **Feature** Added support for using proxy servers with Amazon CodeWhisperer.

## 1.46.0.0 (2023-12-12)

- **Feature** CodeWhisperer suggestions can now be provided for C and C++ files (.c, .h, .cpp, and .hpp extensions)

## 1.45.0.0 (2023-11-22)

- **Breaking Change** From this version on, AWS Toolkit for Visual Studio 2022 requires a minimum Visual Studio version of 17.7.
- **Feature** Added Preview support for Amazon CodeWhisperer - your AI coding companion. See https://aws.amazon.com/codewhisperer/ to learn more.

## 1.44.0.0 (2023-11-14)

- **Bug Fix** Fix a source of "Unknown error converting pem to ppk file" issues when making SSH connections to EC2 instances
- **Deprecation** An upcoming release of the AWS Toolkit for Visual Studio 2022 will require a minimum Visual Studio version of 17.7. An info bar has been added to the Toolkit as a reminder - see https://github.com/aws/aws-toolkit-visual-studio/issues/375 for details.
- **Feature** Added support for Lambda Custom Runtime AL2023 deployment.
- **Feature** Publish to AWS has been updated to use v1.16.7 of the AWS .NET deploy tool. This version of the Toolkit includes the following Deploy Tool changes:
  - Add .NET8 support for Beanstalk web apps and ECS Fargate console apps
  - Add support for .NET8 container-based web apps
  - Add support for NodeJS 18 in generated dockerfiles
  - Improves on some error messaging
  - Uses an updated CDK bootstrap template
  - See https://github.com/aws/aws-dotnet-deploy/releases/tag/1.12.3, https://github.com/aws/aws-dotnet-deploy/releases/tag/1.13.4, https://github.com/aws/aws-dotnet-deploy/releases/tag/1.14.6, https://github.com/aws/aws-dotnet-deploy/releases/tag/1.15.7 and https://github.com/aws/aws-dotnet-deploy/releases/tag/1.16.7 for more details.
- **Feature** Added support for deploying Custom Runtime AL2 functions with Arm64 architecture to AWS Lambda.

## 1.43.0.0 (2023-09-05)

- **Bug Fix** Improvements have been made to the Lambda publish dialog to differentiate between creating a new function and publishing to an existing function. This fixes an issue where typing a function name could cause the function's configuration to be overwritten with a different function's configuration.
- **Bug Fix** Switched to signed version of the underlying cli tool used for zipping Lambda function deployment bundles
- **Feature** AWS Toolkit for Visual Studio is now generally available for Arm64 Visual Studio
- **Feature** The Getting Started experience has been improved, making it easier to add IAM Identity Center authentication to the AWS Toolkit for Visual Studio.

## 1.42.0.0 (2023-06-21)

- **Deprecation** Removed the dotnetcore3.1 runtime from Lambda deployment dialogs. This runtime has reached end of support. See https://docs.aws.amazon.com/lambda/latest/dg/runtime-support-policy.html for more details.
- **Feature** AWS Toolkit for Visual Studio is now available as a Preview for Arm64 Visual Studio. We're interested in hearing about your experience using the Toolkit on Arm systems! Share feedback from the banner shown in the AWS Explorer.

## 1.41.0.0 (2023-05-30)

- **Bug Fix** Fix issue viewing Beanstalk Environments where the Resources tab would not show details. Health check information is no longer displayed in the load balancer details.
- **Bug Fix** Entering a local repo path on the CodeCatalyst Clone Repository dialog now validates the path on changes rather than clicking away from the textbox which did not always work consistently depending on where the user clicked.
- **Bug Fix** Clone CodeCatalyst Repository dialog now only lists repositories that are hosted on CodeCatalyst
- **Bug Fix** Fix "Unable to get IAM security credentials from EC2 Instance Metadata Service." error when trying to clone CodeCatalyst repos on a system that does not contain a default credentials profile.
- **Bug Fix** Fixes issue where the AWS Explorer would sometimes show both the connection status and the resource tree at once.

## 1.40.0.0 (2023-03-10)

- **Feature** Publish to AWS has been updated to use v1.11.6 of the AWS .NET deploy tool. This version fixes an issue where deployed .NET systems would not know the correct heap size. See https://github.com/aws/aws-dotnet-deploy/releases/tag/1.11.6 for more details.

## 1.39.0.0 (2023-02-10)

- **Breaking Change** When connecting to AWS IAM Identity Center (formerly AWS SSO) and AWS Builder ID, it is now necessary to copy a user code from the Toolkit login dialog and paste it into the login page that is opened in the browser. This change helps to ensure that the browser-based login request is associated with actions being performed in the Toolkit.
- **Bug Fix** Before cloning a CodeCatalyst repository, a message is now written to the Output pane stating that a clone will be attempted.
- **Bug Fix** Loading CloudFormation template projects no longer displays a "Target framework not supported" dialog that attempts to target .NET Framework 4.0. The Toolkit now requires .NET Framework 4.7.2 in order to handle these projects.
- **Bug Fix** Fixed issue with Lambda project templates having an invalid region specified in appsettings.Development.json file
- **Bug Fix** AWS IAM Identity Center (AWS SSO) related credentials profiles that are created using the AWS CLI command `aws configure sso` now appear in the Toolkit.
- **Bug Fix** When an error is displayed on the Clone CodeCatalyst Repository dialog, only the error message is shown rather than all exception details.
- **Bug Fix** Improves error message detail on CodeCatalyst cloning failures and ensures the proper Output window pane is displayed to show the error details.
- **Feature** Publish to AWS has been updated to use v1.10.4 of the AWS .NET deploy tool. This version of the Toolkit includes the following Deploy Tool changes:
  - .NET 6 is now required in order to use the publish experience. .NET Core 3.1 was the previously supported minimum version, but this has reached end of life.
  - Error messaging has been improved when deployments fail
  - Security group validations have been improved when publishing to Fargate
  - See https://github.com/aws/aws-dotnet-deploy/releases for more details.

## 1.38.0.0 (2022-12-02)

- **Feature** Added support for cloning Amazon CodeCatalyst source repositories from Visual Studio's 'Clone a Repository' dialog

## 1.37.0.0 (2022-11-07)

- **Breaking Change** The AWS Toolkit now produces log files for each running instance of Visual Studio. This allows concurrent running instances of Visual Studio to have their own unique Toolkit log file. Previously, the first running instance of Visual Studio would append its logs to the same log file. Log files are now produced in `%localappdata%/AWSToolkit/logs/visualstudio/(VisualStudioVersion)`, and are named based on the date and time when Visual Studio was opened.
- **Bug Fix** Beanstalk platform versions can now be configured when deploying to existing Beanstalk targets with Publish to AWS.
- **Bug Fix** Push commands have been updated to use `get-login-password` when viewing an ECR Repository
- **Bug Fix** Fixed issue where Lambda functions could not be published to regions like GovCloud due to "GetFunctionURLConfig does not exist in (region)" error
- **Feature** The Toolkit's Logs can now be accessed from the "AWS Toolkit" menu, located in the "Extensions" menu.
- **Feature** Added support for publishing .NET 7 AOT Lambda functions. To use this, use a Custom Runtime Lambda Project targeting .NET 7, and set the project property `PublishAot` to true
- **Feature** Added local debugging support for .NET 7 Lambda projects using the Lambda Test Tool.
- **Feature** The "Publish to AWS" experience is now capable of publishing .NET 7 applications to Beanstalk using self contained build. This is necessary for Beanstalk images that do not support .NET 7.
- **Feature** Publish to AWS has been updated to use v1.6.4 of the AWS .NET deploy tool. This version of the Toolkit includes the following Deploy Tool changes:
  - Add support for deploying .NET 7 applications to Elastic Beanstalk
  - Allow changing Elastic Beanstalk's platform version for environments
  - See https://github.com/aws/aws-dotnet-deploy/releases/tag/1.6.4 for more details.
- **Feature** Publish to Beanstalk experience now defaults to using self contained deployment bundles for .NET 7 projects. This setting is necessary for Beanstalk images that do not support .NET 7.
- **Removal** CloudFormation Template cost estimator has been removed.

## 1.36.0.0 (2022-10-12)

- **Bug Fix** Configuring a Lambda function to remove all Environment Variables and VPC settings from the Configuration tab of the function's view will now do this. Previously, the Lambda function would be updated, but the function's VPC settings and Environment Variables would not be adjusted.
- **Bug Fix** Update credentials dialog help to link to the User Guide
- **Bug Fix** Fixed bug so that default location, if set in Options, is used when creating or cloning CodeCommit repos rather than always defaulting to %USERPROFILE%\Source\Repos.
- **Feature** The "Publish to AWS" experience is now capable of publishing applications to existing Windows Beanstalk environments
- **Feature** Publish to AWS has been updated to use v1.5.4 of the AWS .NET deploy tool. This version of the Toolkit includes the following Deploy Tool changes:
  - Applications can now be published to existing Windows Beanstalk environments
  - Applications can now be published to Fargate using internet-facing load balancers
  - BlazorWasm applications can now be published with Http3 support
  - See https://github.com/aws/aws-dotnet-deploy/releases/tag/1.3.7, https://github.com/aws/aws-dotnet-deploy/releases/tag/1.4.10, https://github.com/aws/aws-dotnet-deploy/releases/tag/1.5.4 for more details
- **Feature** This release of the Toolkit includes an updated signing certificate, which can be seen when installing the extension.

## 1.35.2.0 (2022-08-24)

- **Bug Fix** Categories are now ordered as intended when editing settings in Publish to AWS.
- **Bug Fix** Publish to AWS has been updated to use v1.2.4 of the AWS .NET deploy tool. This version of the Toolkit includes the following Deploy Tool changes: https://github.com/aws/aws-dotnet-deploy/releases/tag/1.2.4 , https://github.com/aws/aws-dotnet-deploy/releases/tag/1.1.15 .
- **Bug Fix** A bug has been fixed in Publish to AWS when publishing a project to an existing Fargate target, where the Fargate target was previously published using a pre-GA version of Publish to AWS. If the target was configured with multiple security groups, trying to select it would log an 'Unexpected character encountered while parsing value: s.' error. Now, you can re-publish your project to this target, but you need to reconfigure the security groups setting. The setting will display a validation message in the 'Edit Settings' view if reconfiguration is needed. (Fixed in Deploy Tool v1.1.15)
- **Bug Fix** Fix issue preventing Publish to AWS from publishing to a Fargate target when working with a region that does not have a default VPC. Previously, this would log an `Unexpected character encountered while parsing value: s. Path '', line 0, position 0` error (Fixed in Deploy Tool v1.2.4)
- **Feature** Searching CloudWatch log events has been improved, so that filtered events are automatically loaded. Previously, you would have to occasionally click on a link in order to retrieve the first screenful of events.

## 1.35.1.0 (2022-07-25)

- **Bug Fix** CodeArtifact NuGet credential provider has been improved to reduce the amount of times it falls back to a standard basic authentication dialog.
- **Bug Fix** Fixes bug that attempted to set ACLs on S3 buckets that don't support ACLs.  This was seen in the S3 object browser as an error message from operations such as rename and copy/paste."
- **Bug Fix** Fix Lambda project template not detecting Node.js tools properly and displaying error message.
- **Bug Fix** Display error message in Publish to AWS when the Deploy Tool fails to load configuration for a target. This used to leave the Publish button enabled, but it would not do anything.
- **Bug Fix** Fix bug where AWS Explorer would cause multiple AWS MFA and AWS SSO Login prompts to appear, even when cancelled
- **Bug Fix** Fixes bug where uploading a file to the root of an S3 Bucket actually uploads to a no-name folder at root.
- **Bug Fix** Fix issue where downloading a CloudWatch log stream would occasionally never complete.

## 1.35.0.0 (2022-07-05)

- **Feature** The Publish to AWS experience is now generally available
- **Feature** Publish to AWS has been updated to use v1.0.3 of the AWS .NET deploy tool (https://github.com/aws/aws-dotnet-deploy/releases/tag/1.0.3). This release is also generally available, and includes validation checks for configuring Managed Platform Update times when deploying to Beanstalk.

## 1.34.0.0 (2022-06-30)

- **Breaking Change** Publish to AWS now requires a minimum NodeJs version of 14. Previously, this was 10.
- **Bug Fix** Fix "Assembly AWSSDK.SSOOIDC could not be found or loaded. This assembly must be available at runtime to use Amazon.Runtime.SSOAWSCredentials" error introduced in Toolkit version 1.32.0.0. This prevented the Toolkit from working with SSO based credentials.
- **Feature** Publish to AWS is now capable of publishing Elastic Beanstalk running on Windows images
- **Feature** Publish to AWS has been updated to use v0.50.2 of the AWS .NET deploy tool. This includes https://github.com/aws/aws-dotnet-deploy/releases/tag/0.50.2, https://github.com/aws/aws-dotnet-deploy/releases/tag/0.49.14, and https://github.com/aws/aws-dotnet-deploy/releases/tag/0.48.15
- **Feature** Add workaround for Publish to AWS when running on a system that has a space in the user profile's path. See https://aws.github.io/aws-dotnet-deploy/docs/getting-started/custom-workspace/ for details

## 1.33.0.0 (2022-06-29)

- **Bug Fix** Fixes issues with navigating, copying, and pasting to/from S3 paths that contain no-name directories.  See https://github.com/aws/aws-toolkit-visual-studio/issues/248
- **Feature** A link to the Troubleshooting Guide is now shown in the Publish to AWS experience when a deployment fails.
- **Feature** Amazon CloudWatch Logs Support: View, filter and store CloudWatch Logs resources from the AWS Explorer.
- **Feature** Added support to view CloudWatch Logs for Lambda functions and ECS Tasks.

## 1.32.0.0 (2022-06-17)

- **Feature** Publish to AWS has been updated to use v0.47.26 of the AWS .NET deploy tool. It contains new validation checks to help prevent deployment failures - https://github.com/aws/aws-dotnet-deploy/releases/tag/0.47.26

## 1.31.0.0 (2022-06-07)

- **Bug Fix** Fix scenario in Publish to AWS where invalid setting values would revert to a previous valid value while the settings were still being edited.
- **Feature** Adds a Browse button to the Publish to AWS targets that allow for Dockerfile paths. This opens a file dialog to allow the user to browse to and select the Dockerfile to be used in the deployment.
- **Feature** Add Publish to AWS validation checks for scenarios where a deployment could conflict with existing account resources.
- **Feature** Add Publish to AWS validations to check that references to existing IAM Roles are not left empty

## 1.30.0.0 (2022-06-01)

- **Bug Fix** Fix issue where clicking different targets in the Publish to AWS experience could show the configuration for an older selection
- **Bug Fix** Fix issue in Publish to AWS where Docker and Build settings were not used during the publish.
- **Feature** Add Publish to AWS validation check for scenario where a new deployment would re-use the name of an existing deployment.
- **Feature** Updated the Publish to AWS view where deployment targets are listed, so that more of the list can be displayed on the screen.
- **Feature** Updated the Publish to AWS view where deployment settings can be edited. Settings are grouped by category, and a side-bar allows for quick navigation to a category. The width of this view has also been constrained, so that it is easier to work with on systems with a wider display.

## 1.29.0.0 (2022-05-16)

- **Bug Fix** Fix DynamoDB Local connection failure when using a non-basic default credentials profile (SSO or MFA for example)
- **Bug Fix** Configuring the Lambda publish wizard to remove all VPC subnets and security groups from an existing Lambda will now do this when publishing to Lambda. Previously, the Lambda function would be updated, but the function's VPC settings would not be adjusted.
- **Feature** The Publish to AWS experience now indicates if the Application Name is not valid, and prevents a deployment from starting.
- **Feature** Add support for configuring VPC Connectors when publishing to App Runner through the Publish to AWS experience.
- **Feature** When configuring roles in the Publish to AWS experience, if the publish target requires a service principal, the role selection dialog will only show roles that reference the service principal.

## 1.28.0.0 (2022-04-12)

- **Breaking Change** From this version on, the Toolkit no longer supports Visual Studio 2017.
- **Bug Fix** Fix problem where dropdown controls would not open, and UI controls would flicker when shown on secondary displays. This mostly affected the Publish to AWS settings screen.
- **Bug Fix** Fixes case where the Publish to AWS summary screen was unable to open the CloudFormation stack viewer for a profile/region combination that did not match what is currently selected in the AWS Explorer.
- **Feature** Add support for publishing .NET 6 applications to Linux based Beanstalk images in the Publish to AWS experience
- **Feature** The Publish To Beanstalk experience no longer defaults to using self-contained deployment bundles when publishing .NET 6 projects to Linux images.
- **Feature** Publish to AWS experience can now publish images to ECR Repositories

## 1.27.0.0 (2022-03-23)

- **Bug Fix** Editing Beanstalk environment values now ignores entries with empty keys in the Publish to AWS experience.
- **Bug Fix** Fix Publish Container to AWS wizard so that the Schedule Rule Type is correctly restored as Fixed/Cron with the correct expression.
- **Bug Fix** Fix showing CloudFormation stack after Publish to AWS completes.
- **Bug Fix** Fix issue where AWS Explorer button images would not display
- **Deprecation** An upcoming release will remove support for Visual Studio 2017. An info bar has been added to the Toolkit as a reminder - see https://github.com/aws/aws-toolkit-visual-studio/issues/221 for details.
- **Feature** The wizard for publishing Lambda projects and Serverless application projects now defaults to the Credentials profile and region from `aws-lambda-tools-defaults.json`. If these values are not found, the current AWS Explorer values are used.
- **Feature** Added a way to configure the Credentials and region used when publishing with the "Publish to AWS" experience.
- **Feature** Added menu items to view the '.NET on AWS' and '.NET on AWS Community' websites, available from the "AWS Toolkit" menu, located in the "Extensions" menu ("Tools" menu in Visual Studio 2017)

## 1.26.0.0 (2022-02-23)

- **Bug Fix** Added link to view the Beanstalk environment when publishing to existing Beanstalk environments with the "Publish to AWS" experience
- **Feature** Add support for publishing Lambda functions using the .NET 6 managed runtime
- **Feature** Visual Studio 2022 Lambda project blueprints have been updated to target .NET 6.

## 1.25.0.0 (2022-02-17)

- **Bug Fix** The Toolkit Output channel no longer takes focus when credentials profiles are reloaded
- **Bug Fix** "Publish to AWS" experience now supports new regions like Jakarta
- **Bug Fix** Fix issue with icons not correctly handling the dark theme in Visual Studio 2022.
- **Bug Fix** Fixed bug where the "Publish to AWS" experience would not work for users with a space in their Windows profile path
- **Feature** Beanstalk environment variables can now be configured in the "Publish to AWS" experience
- **Feature** Added more validation checks to ECS Fargate and App Runner based targets in the Publish to AWS experience
- **Feature** Menu items for the new (preview) "Publish to AWS" experience and the older publishing experiences are no longer mutually exclusive.
- **Feature** Improved the "Publish to AWS" experience for configuring EC2 Instance Types by adding a selection dialog.
- **Feature** The "Publish to AWS" experience is now capable of publishing applications to existing Beanstalk environments
- **Feature** Added support for credential profiles that use `role_arn` and `credential_source`, where `credential_source = Ec2InstanceMetadata`. This makes it easier to use the Toolkit from within a Windows EC2 instance, since it isn't necessary to place account secrets in the credentials file on the instance.

## 1.24.0.0 (2021-12-20)

- **Bug Fix** Fix issue in the Lambda publish dialog that would prevent it from showing the list of Lambda functions in an account.
- **Bug Fix** Fix "An update is in progress for resource" failure when publishing NodeJs Lambda functions
- **Bug Fix** If the new "Publish to AWS" experience has a problem starting up, it attempts to enable the older publishing experience.
- **Bug Fix** The Toolkit now shows a message if Credentials are not valid when trying to open the new "Publish to AWS" experience.
- **Feature** Added .NET 6 Lambda container images to the Lambda project blueprints for Visual Studio 2022
- **Feature** The AWS Toolkit for Visual Studio 2022 is now out of Preview.
- **Feature** Add support for configuring Lambda Test Tool for .NET 6 projects
- **Feature** Updated the charts in the Monitoring panel of Beanstalk Environments and CloudFormation stacks. This addresses the "DataVisualization.Charting" error that could happen when trying to view Environments.
- **Feature** Improved the "Publish to AWS" experience for configuring VPCs and IAM Roles. Existing resources can be selected from a dialog.

## 1.23.3.0 (2021-11-17)

- **Bug Fix** Added support for CloudFormation Template projects into the Visual Studio 2022 Toolkit.
- **Feature** Add option in the Publish to Beanstalk workflow to build self-contained deployment bundles, when working with .NET Core/.NET 5+ applications and Windows images. This enables .NET 6 projects to be published to Windows servers using the Publish to Beanstalk feature.
- **Feature** Make Publish to Beanstalk experience default to using self contained deployment bundles for .NET 6 projects. This setting is necessary for Beanstalk images that do not contain the .NET 6 runtime.

## 1.23.2.0 (2021-11-12)

- **Bug Fix** Added the CodeArtifact NuGet Credentials provider into the Visual Studio 2022 Toolkit.
- **Feature** Added Lambda Blueprints for .NET 6 based Custom Runtime Functions to Visual Studio 2022
- **Feature** Improved solution load times by installing Lambda Test Tool asynchronously with it's progress status visible in Task Status Center.

## 1.23.1.0 (2021-11-04)

- **Feature** Adding hyperlink to help guide installation of missing system dependencies in the New Publish Experience.
- **Feature** A preview version of the AWS Toolkit is now available for Visual Studio 2022 from the Marketplace. It is a separate extension from the AWS Toolkit for Visual Studio 2017 and 2019. Not all of the Toolkit functionality is available in this version - see https://github.com/aws/aws-toolkit-visual-studio/issues/167 for details.

## 1.23.0.1 (2021-10-26)

- **Feature** This release of the Toolkit includes an updated signing certificate, so that the VSIX installation process does not show an error message.

## 1.23.0.0 (2021-10-21)

- **Bug Fix** Fixed an issue where autocompletion in CloudFormation templates would replace too much text
- **Deprecation** Removed the dotnetcore2.1 runtime from Lambda deployment dialogs. This runtime has reached end of support. See https://docs.aws.amazon.com/lambda/latest/dg/runtime-support-policy.html for more details.
- **Feature** A new, simplified experience for publishing your .NET applications to AWS is now available as a preview feature within Visual Studio 2019. This experience is based on the AWS .NET deployment tool (https://github.com/aws/aws-dotnet-deploy), and gives you publishing recommendations based on your application. This new experience can be enabled from the existing Beanstalk and Container publishing dialogs. For more details, see https://aws.amazon.com/blogs/developer/simplify-dotnet-publication-toolkit/ and https://docs.aws.amazon.com/toolkit-for-visual-studio/latest/user-guide/publish-experience.html
- **Feature** Icons for AWS services have been updated throughout the Toolkit.

## 1.22.0.0 (2021-09-29)

- **Bug Fix** Fixed an issue where the Import CSV button on the Getting Started page showed no results  
- **Bug Fix** Fix issue of only showing one page of IAM resources in AWS explorer
- **Deprecation** Removed the nodejs10.x runtime from Lambda deployment dialogs. This runtime has reached end of support. See https://docs.aws.amazon.com/lambda/latest/dg/runtime-support-policy.html for more details.
- **Feature** Added a menu item to submit quick toolkit feedback, available from the "AWS Toolkit" menu, located in the "Extensions" menu ("Tools" menu in Visual Studio 2017)
- **Feature** Lambda ARM Support: Deploy .NET Core 3.1 Lambda ARM functions to AWS Lambda.
- **Feature** Added support for Lambda Custom Runtime (AL2) deployment.
- **Feature** Lambda ARM Support: Deploy Zip-based Node.js 12 Lambda ARM functions to AWS Lambda.
- **Feature** The Toolkit's Getting Started Guide can now be accessed from the "AWS Toolkit" menu, located in the "Extensions" menu ("Tools" menu in Visual Studio 2017)

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
