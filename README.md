# sealed-secrets-demo

ingress subdomain name is not hardcoded so lets use poorman's helm (envsubst)
```
 kubectl apply -k https://github.com/lalyos/sealed-secrets-demo \
   --dry-run -o yaml \
   | envsubst \
   | k apply -f -
 ```
