# application-parent
_Parent to all Maven applications_

This POM inherits from the [Parent](https://github.com/varunmc/parent) and enables Spring Boot for all child projects.

## Getting Started
The [AWS CodeFormation](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stack/detail?stackId=arn:aws:cloudformation:us-east-1:497513737772:stack%2FApplicationParent%2F80176970-92ea-11e7-9aeb-500c28b4b099) template _stack.yml_ will create an [AWS CodePipeline](https://console.aws.amazon.com/codepipeline/home?region=us-east-1#/view/ApplicationParent) with an [AWS CodeBuild](https://console.aws.amazon.com/codebuild/home?region=us-east-1#/projects/ApplicationParent/view) builder as defined in _buildspec.yml_. The builder executes `mvn deploy` which will package and publish the artifact to [AWS S3](https://s3.console.aws.amazon.com/s3/buckets/maven.varun.mc/mc/varun/application/parent/?region=us-east-1&tab=overview).

## Pre-Requisites
* Set up the [Parent](https://github.com/varunmc/parent) project
