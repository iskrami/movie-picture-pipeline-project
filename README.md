# movie-picture-pipeline-project

eksctl create cluster --name movie-picture-cluster --region us-east-1 --nodegroup-name my-nodes --node-type t3.small --nodes 1 --nodes-min 1 --nodes-max 2

aws eks --region us-east-1 update-kubeconfig --name movie-picture-cluster

eksctl delete cluster --name movie-picture-cluster --region us-east-1


aws sts assume-role --role-arn arn:aws:iam::425586105601:user/nano-admin --role-session-name YourSessionName --query Credentials.SessionToken --output text
