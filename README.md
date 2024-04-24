# Dagger Snyk module

Known to work with Dagger v0.9.8 only (for v0.9.5 support, see v0.1.0 release).

Check code, infrastructure-as-code and containers using Snyk from your Dagger pipelines.

```
export SNYK_TOKEN=<your-snyk-token>
```

Get this from your [Snyk Account page](https://app.snyk.io/account).


## Code

Check the code in the current directory for vulnerabilities:

```
dagger call -m github.com/daggerverse/dagger-snyk test-code --src . --token env:SNYK_TOKEN
```


## Infrastructure-as-Code

Check the infrastructure-as-code (e.g. Terraform etc) in the current directory for issues:

```
dagger call -m github.com/daggerverse/dagger-snyk test-iac --src . --token env:SNYK_TOKEN
```


## Containers

Check the given container image for vulnerabilities:

```
dagger call -m github.com/daggerverse/dagger-snyk test-container --image "alpine:latest" --token env:SNYK_TOKEN
```