# codebuild-AMI-builder

AWS CodeBuild uses containers to execute the project’s build instructions and build your project.

The buildspec.yml file will use HashiCorp Packer to execute a template and generate an Amazon EC2 AMI. There is no binary output or build result that will be used as an artifact.

In the Service Role section the service role you select here will provide the AWS CodeBuild container with permissions to your AWS account. HashiCorp Packer needs permissions to create a temporary EC2 instance and an AMI, delete an EC2 instance, and perform other EC2-related actions. 

The next step is to create the HashiCorp Packer template and build specification. 

- The HashiCorp Packer template, amazon-linux_packer-template.json.
- The AWS CodeBuild configuration file, buildspec.yml.
___
