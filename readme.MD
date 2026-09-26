OpenID Connect create
```
eksctl utils associate-iam-oidc-provider --cluster roboshop-dev --approve
```

# service account creation
``` 
eksctl create iamserviceaccount \
  --cluster=roboshop-dev \
  --namespace=roboshop \
  --name=secret-reader \
  --attach-policy-arn=arn:aws:iam::051826708837:policy/RoboShopMySQLSecretreader \
  --approve
````