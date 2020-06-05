
```
oc new-app java:8~https://github.com/snandakumar87/sd-product-deployment --name=sd-product-deployment 
--build-env=NEXUSREPO="http://nexus-nexus.apps.cluster-cc6c.cc6c.example.opentlc.com"

```
Build environment will need to be passed in with the URL for the nexus repo.

```
oc expose svc/sd-product-deployment
```

Swagger can be found at: ```{URL}/swagger-ui```

Sample Request for Create Product Deployment
```
POST<product-deployment-url>/service/product-deployment/SD23234/product-or-service-deployment-project/creation

{
  "status": "SUCCESS",
  "data": {
    "productOrServiceDeploymentProjectInstanceReference": null,
    "productOrServiceDeploymentProjectCreateActionReference": null,
    "productOrServiceDeploymentProjectCreateActionRecord": null,
    "productOrServiceDeploymentProjectInstanceStatus": null,
    "crCustomerProductDeploymentInstanceRecord": {
      "customerReference": "720996",
      "productType": "e-wallet",
      "status": "SUCCESS"
    }
  },
  "errors": null
}
```