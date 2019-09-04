# zikalino/azure-sdk-tools

## Using as a standalone container

	docker run -it --rm zikalino/azure-sdk-tools

You may need to call **git pull** to make sure repositories are up to date.

## Using with your local repositories 

	docker run -it --rm -v c:\dev\autorest.cli:/autorest.cli -v c:\dev\azure-rest-api-specs:/azure-rest-api-specs -v c:\dev\generated:/generated --entrypoint bash zikalino/azure-sdk-tools

## Generating Swagger Integration Tests

	autorest --cli --use=/autorest.cli --swagger-integration-test --python-sdks-folder=/generated --output-folder=/generated /azure-rest-api-specs/specification/healthcareapis/resource-manager/readme.md
