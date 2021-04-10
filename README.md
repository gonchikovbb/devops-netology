Files will be ignored:
Terraform local directories
.tfstate files
Crash log files crash.log
tfvars files, which can contain the data being sent, such as password, private keys, and other secrets.
override files as they are usually used to override resources locally and therefore not checked override.tf override.tf.json
override files you want to add to version control using negative pattern! example_override.tf
tfplan files to ignore command plan output: terraform plan -out = tfplan
CLI config files .terraformrc terraform.rc
new line
new line -> with PyCharm
