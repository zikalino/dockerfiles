# Azure CLI + azdev Environment

I have created this one to be able to use most recent **azdev** with **Azure CLI**.
It can be used to run standalone tests.

Running container:

	docker run -it --rm -v c:\dev\cnt:/cnt zikalino/azdev


To be able to run my standalone test I have modified **latest.json** file:

	vi /root/.azdev/env_config/env/test_index/latest.json

where I have added:

	{ "mytest": "/cnt/integration.py" }


Running test:

	azdev test mytest 



