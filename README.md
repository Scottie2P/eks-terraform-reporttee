# eks-terraform-reporttee

1.  install terraform

  ```
  brew reinstall terraform
  ```

2. setup terraform project and run pipeline
  
  ```
    terraform init
    terraform validate
    terraform plan -out tfplan
    terraform apply tfplan 
  ```

  3 connect cluster EKS 

  ```
  aws eks --region $(terraform output -raw region) update-kubeconfig --name $(terraform output -raw cluster_name)
  ```
