# cryptonodes

Install sawtooth.

* Create new server and make sure python installed.
Update inventory/nodes with server IP.

* Invoke deployment
```
$ ansible-playbook -i inventory/nodes --key-file=~/.ssh/crowdNurse_2016 sawtooth-install.yaml
```

* Run on server
```
$ docker-compose -f sawtooth.yaml up -d
```

* See logs
```
$ docker-compose -f sawtooth.yaml logs
```

* Shutdown
```
$ docker-compose -f sawtooth.yaml stop
```
then to remove all server instance
``` 
$ docker-compose -f sawtooth.yaml down 
```

See also: https://sawtooth.hyperledger.org/docs/core/releases/1.0/app_developers_guide/docker.html#logging-into-the-client-container