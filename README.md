# Skeleton for creation of IBM Cloud Schematics blueprint templates  

This repository contains a sample blueprint template and input file that can be used as a basis to create your own custom blueprints. It contains two files. 

- `sample-template-blueprint.yaml` - A skeleton template containing two module definitions that can be customized to deploy your Terraform automation configs and modules. 
- `sample-input.yaml` - An input file pre-populated with input values for the sample template  


## Editing the sample template in VSCode

The editing and validation of blueprint templates in VSCode utilizes the Red Hat VSCode YAML extension from the [VSCode Marketplace](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml) with a blueprint [JSON-Schema](json-schema.org). Follow the YAML language extension and blueprint schema [installation and configuration instructions](https://github.com/Cloud-Schematics/vscode-blueprint-schema) to configure your VSCode environment.     

### Clone template repo in Git
To use this example to create your own blueprint template in VSCode, first create a copy of this template in your own Git repository or version control system. These instructions refer to the use with Github: 
- Navigate to the main page of this repository  
- Click **Use this template** 
- Select **Create a new repository** 
- Use the Owner drop-down menu, and select the account where want to create the new repository
- Type a name for your repository
- Click **Create repository from template**

### Clone repo to local machine
Clone your new template repository to your local machine for editing:
- Navigate to the main page of your new repository
- Click **<> Code** (Download Code)
- [Clone the repo](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) to your local machine using: HTTPS, SSH, GitHub CLI or Github Desktop

### Editing in VSCode
- Open the local folder containing the template repo contents as a new VSCode workspace
- Optionally rename the template and input files for your blueprint. 
- Select the file `sample-template-blueprint.yaml` for editing
- Just above the top of the file contents, the selected schema is displayed.  
![Blueprint template schema](images/vscode-schema-banner.png)  

With the extension and schema configured, VSCode will provide assisted editing for blueprint templates.

### Blueprint usage and configuration documentation
To customize the template to deploy your own infrastructure, refer to the Blueprint documentation for an overview of [blueprint templates and configuration](https://cloud.ibm.com/docs/schematics?topic=schematics-blueprint-templates&interface=ui). 

To start on editing the template and inputs, then deploying the blueprint, follow the steps laid out in [Defining Blueprints](https://cloud.ibm.com/docs/schematics?topic=schematics-define-blueprints). 



## Blueprint template - sample-template-blueprint.yaml

This sample template links two Terraform configs as modules.

Replace all enclosed text, <module_1>, <output_1> with values for your modules.  

The TF configs used in this blueprint are sourced from the repo https://github.com/Cloud-Schematics/blueprint-example-modules/
```
Blueprint file: sample-template-blueprint.yaml
├── module_1
|    └── source: github.com/Cloud-Schematics/blueprint-example-modules
└── module_2
     └── source: github.com/Cloud-Schematics/blueprint-example-modules
```

### Blueprint template inputs 
The sample-template-blueprint.yaml template file accepts the following inputs:

| Name | Type | Value | Description |
|------|------|------|----------------|
| variable_1 | string |  |  |
| variable_2 | string |  |  |

### Blueprint outputs
The sample-template-blueprint.yaml template creates the following outputs:

| Name | Type | Value | Description |
|------|------|------|----------------|
| <outputs_1> | string |  |  |
| <outputs_2> | string |  |  |

## Blueprint input file sample-template-input.yaml
The input file defines the variable names and values for the required blueprint template inputs. 

| Name | Type | Value | Description |
|------|------|------|----------------|
| cos_instance_name | string | blueprint-basic  | Name for COS instance |
| cos_storage_plan | string | lite | Service plan type for COS instance |


## Example blueprint templates

Deployable template examples can be found in the [IBM Cloud Schematics GitHub repository](https://github.com/orgs/Cloud-Schematics/repositories/?q=topic:blueprint). 