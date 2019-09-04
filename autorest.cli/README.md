# zikalino/autorest.cli

## Using Container

	docker run -it --rm -v c:\dev\autorest.cli:/autorest.cli -v c:\dev\azure-rest-api-specs:/azure-rest-api-specs -v c:\dev\generated:/generated --entrypoint bash zikalino/autorest.cli

## Integration Tests

	autorest --cli --use=/autorest.cli --swagger-integration-test --python-sdks-folder=/generated --output-folder=/generated /azure-rest-api-specs/specification/healthcareapis/resource-manager/readme.md