# Ec2-instance-module-for-jenkins-and-sonarqube

This module set up the build of **JENKINS** and **SONARQUBE** instance.

This module was built using [koji-cookiecutter-microservice](git@github.com:Bkoji1150/ec2-instance.git).
<!-- prettier-ignore-start -->
<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.1.4 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >=3, <4 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | 3.74.0 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_Sonarqube_instance"></a> [Sonarqube\_instance](#module\_Sonarqube\_instance) | ./module/ec2instance-jenkins-sonarqube | n/a |
| <a name="module_jenkins_instance"></a> [jenkins\_instance](#module\_jenkins\_instance) | ./module/ec2instance-jenkins-sonarqube | n/a |

## Resources

| Name | Type |
|------|------|
| [aws_iam_instance_profile.ec2_profile](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_instance_profile) | resource |
| [aws_iam_policy.ec2_policy](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_policy) | resource |
| [aws_iam_policy_attachment.ec2_policy_role](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_policy_attachment) | resource |
| [aws_iam_role.ec2_role](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role) | resource |
| [aws_key_pair.key](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/key_pair) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_ami"></a> [ami](#input\_ami) | ami id specific only to for jenkins/sonarqube build in us-east-1 | `string` | `"ami-0a8b4cd432b1c3063"` | no |
| <a name="input_aws_region"></a> [aws\_region](#input\_aws\_region) | The region with which this template would be deployed | `string` | `"us-east-1"` | no |
| <a name="input_instance_type"></a> [instance\_type](#input\_instance\_type) | Instance type for both jenkins instance and sonarqube | `string` | `"t2.medium"` | no |
| <a name="input_jenkins_name"></a> [jenkins\_name](#input\_jenkins\_name) | instance name for jenkins instance | `string` | `"JenkinsMaster"` | no |
| <a name="input_public_key_path"></a> [public\_key\_path](#input\_public\_key\_path) | local keypair | `string` | `"/Users/kojibello/.ssh/id_rsa.pub"` | no |
| <a name="input_sonarqube_name"></a> [sonarqube\_name](#input\_sonarqube\_name) | instance name for sonarqube instance | `string` | `"Sonarqube"` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_jenkins_public_ip"></a> [jenkins\_public\_ip](#output\_jenkins\_public\_ip) | below is the jenkins instance ipp |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
<!-- prettier-ignore-end -->

## Authors

Module is maintained by [Koji Bello](https://github.com/Bkoji1150) with help from [these awesome contributors](https://github.com/terraform-aws-modules/terraform-aws-ec2-instance/graphs/contributors).
