# Business Use Case

The CMDT record defines the implementation class for an interface.  During normal business logic the canonical class would perform the desired logic, e.g. callout to an external service.  However in a pre-production scratch orgs or sandboxes, the external service callout is not permissible, therefore a stand-in implementation is needed, which is defined in an overriding CMDT record to be deployed.

## Desired Steps
 
1. 'source:push' canonical application metadata, residing under 'sfdx-source/cmdt-deploy-investigation'.
2. 'source:deploy' the stand-in logic, residing under 'sfdx-source-supplements/cmdt-deploy-investigation-additions'.

## Expectation

After 'source:deploy', a single CMDT record exists having 'Implementation Class' with the value of 'StandinBusinessLogic'.