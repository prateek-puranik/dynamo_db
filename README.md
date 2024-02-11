DynamoDB
============================

### Directory layout

    .dynamodb_table/
    ├── main.tf                   # Create the dynamodb tables and table items  
    ├── locals.tf                 # Load JSON data from json files
    ├── providers.tf              # For specifying the terraform, aws versions and access keys
    ├── config.json               # Contains data from ConfigTable in JSON format
    ├── news.json                 # Contains data from NewsTable in JSON format
    └── stockprice.json           # Contains data from StockPrice_Sentiment_Table in JSON format
    



### Step 1: Initialize Terraform
`terraform init`

### Step 2: Enter Access Key and Secret Key in providers.tf
Update the access and secret keys in the 'providers.tf' file.

### Step 3: Generate Terraform execution plan
`terraform plan`
Verify that no errors are reported.

### Step 4: Apply the Terraform configuration
`terraform apply`
Confirm deployment by typing 'yes' and ensure no errors occur.

