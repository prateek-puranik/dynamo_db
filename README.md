ECS task definition + Scheduled task
============================

### Directory layout

    .
    ├── main.tf                   # File defines the Eventbridge Rules and Targets 
    ├── task_defintion.tf         # File defines the ECS Task Defintions using a for_each loop
    ├── variables.tf              # File contains the variables 
    ├── test                    # Automated tests (alternatively `spec` or `tests`)
    ├── tools                   # Tools and utilities
    ├── LICENSE
    └── README.md

> Use short lowercase names at least for the top-level files and folders except
> `LICENSE`, `README.md`
