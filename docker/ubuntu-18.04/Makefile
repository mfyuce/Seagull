.PHONY: build
build:
	docker build -t localhost/seagull:ubuntu1804 .

.PHONY: run
run:
	docker run -p 3868:3868 -v /home/netas/projects/scef-test/seagull/diameter/logs:/opt/seagull/diameter/logs -v /home/netas/projects/scef-test/seagull/config/:/opt/seagull/config -v /home/netas/projects/scef-test/diameter:/opt/seagull/diameter -i -t --rm --detach --name seagull-ubuntu1804 localhost/seagull:ubuntu1804 /bin/bash || :

.PHONY: exec
exec:
	docker exec -it seagull-ubuntu1804 /bin/bash

.PHONY: stop
stop:
	docker stop seagull-ubuntu1804 || :
