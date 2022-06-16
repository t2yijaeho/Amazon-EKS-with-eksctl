# Launching Amazon EKS Cluster with eksctl


## 1. Prepare Environment

Refer to [AWS Cloud9](https://github.com/t2yijaeho/Docker-with-AWS-Cloud9)


## 2. Install eksctl

Refer to [Installing eksctl](https://docs.aws.amazon.com/eks/latest/userguide/eksctl.html)

[eksctl GitHub Pages](https://eksctl.io/)

1. Download and extract the latest release of `eksctl`

    ```console
    curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
    ```
    
    ```console
    mspuser::~/environment $ curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
    mspuser::~/environment $ 
    ```

2. Move the extracted file to binary directory

    ```console
    sudo mv /tmp/eksctl /usr/local/bin
    ```
    
    ```console
    mspuser::~/environment $ sudo mv /tmp/eksctl /usr/local/bin
    mspuser::~/environment $ 
    ```
    
3. Verify `eksctl` version

    ```console
    eksctl version
    ```
    
    ```console
    mspuser::~/environment $ eksctl version
    0.101.0
    mspuser::~/environment $ 
    ```
    
## 3. Launch EKS cluster

1. Launch EKS cluster and node groups on AWS Fargate

    ```console
    eksctl create cluster --name K8sBasics --fargate
    ```
    
    ```console
    mspuser::~/environment $ eksctl create cluster --name K8sBasics --fargate
    mspuser::~/environment $ 
    ```

2. Launch EKS cluster and node groups on Amazon EC2 instance
