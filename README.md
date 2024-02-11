ECS task definition + Scheduled task
============================

### Directory layout

    .ecs_simplified/
    ├── main.tf                   # File defines the Eventbridge Rules and Targets 
    ├── task_defintion.tf         # File defines the ECS Task Defintions using a for_each loop
    ├── variables.tf              # File contains the variables needed in task_defintion.tf
    ├── IAM_policy.tf             # The IAM role and inline policy for task_definitions and 
    |                              Eventbridge Rules
    ├── IAM_Tasks.tf              # IAM role assignment to ECS Tasks on access to AWS resources
    ├── log_groups.tf             # For creating the log groups for Scheduled ECS Tasks
    ├── vpc.tf                    # Contains the configuration of the subnets and security groups
    └── providers.tf              # For specifying the terraform version and aws version



### Step 1: Initialize Terraform
`terraform init`

### Step 2: Enter Access Key and Secret Key in main.tf
Update the access and secret keys in the 'main.tf' file.

### Step 3: Generate Terraform execution plan
`terraform plan`
Verify that no errors are reported.

### Step 4: Apply the Terraform configuration
`terraform apply`
### Confirm deployment by typing 'yes' and ensure no errors occur.

### Step 5: Update EC2 instance settings
#### - Navigate to EC2 Instances -> Instances.
#### - Select the Fabric NAT CheckBox.
#### - Go to Actions -> Networking -> Change Source / destination check.
#### - Check the Stop Checkbox.
