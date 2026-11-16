cd ~/devops-project/infra
cat > README.md <<'EOF'
# devops-demo-infra

Terraform code that creates a 3-node Kubernetes cluster (1 control-plane, 2 workers)
on my laptop using kind and Docker.

## Usage
    terraform init
    terraform plan
    terraform apply
    export KUBECONFIG=$(terraform output -raw kubeconfig_path)
    kubectl get nodes

## Cleanup
    terraform destroy
EOF
git add README.md
git commit -m "Add README"
git push
