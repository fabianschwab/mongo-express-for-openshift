# Mongo Express for IBM Databases for MongoDB SaaS

This repository gives you a guide how to set up Mongo Express UI in an OpenShift cluster.
Prerequisites are that an IBM Cloud Databases for MongoDB instance is already set up and you have created your service credentials.

Replace your environment variables with you well use from your service credentials and follow the steps below.

## Setup

### Certificate

When creating your certificate secret be aware that there must be a newline character at the end of the file.
The easiest way is to save your certificate in the `cert.pem` file and be sure that your editor is not removing the new line on save.

Then with the `oc` cli run to create the configMap.

```sh
oc create configmap sslcert --from-file=cert.pem
```

### Deploy

To create the

- Deployment
- Service
- Route

run

```sh
oc apply -f .
```
