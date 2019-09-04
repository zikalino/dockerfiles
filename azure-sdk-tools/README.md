# zikalino/azure-sdk-tools

## Using as a standalone container

	docker run -it --rm zikalino/azure-sdk-tools

You may need to call **git pull** to make sure repositories are up to date.

## Using with your local repositories 

	docker run -it --rm -v c:\dev\autorest.cli:/autorest.cli -v c:\dev\azure-rest-api-specs:/azure-rest-api-specs -v c:\dev\generated:/generated --entrypoint bash zikalino/azure-sdk-tools

or

	docker run -it --rm -v c:\dev\azure-rest-api-specs:/azure-rest-api-specs -v c:\dev\generated:/generated --entrypoint bash zikalino/azure-sdk-tools

if you want to use **autorest.cli** released as an NPM package

## Generating Swagger Integration Tests

Using **autorest.cli** from local folder:

	autorest --cli --use=/autorest.cli --swagger-integration-test --python-sdks-folder=/generated --output-folder=/generated /azure-rest-api-specs/specification/healthcareapis/resource-manager/readme.md

Using **autorest.cli** from NPM package:

	autorest --cli --use="autorest.cli@~0.1.1" --swagger-integration-test --python-sdks-folder=/generated --output-folder=/generated /azure-rest-api-specs/specification/healthcareapis/resource-manager/readme.md

