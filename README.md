# Cert issuer
Helm chart providing cert issuer resources

# Package
```bash
helm package --sign --key helm --keyring ~/.gnupg/pubring.gpg .
```

# Push
```bash
export AWS_DEFAULT_REGION=eu-west-1
helm s3 push ./cert-issuer-0.1.0.tgz dhis2
aws s3 cp cert-issuer-0.1.0.tgz.prov s3://helm.dhis2.org/stable/
```
