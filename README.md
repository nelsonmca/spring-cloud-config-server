##   Config server


[![D|Solid](https://www.currenciesdirect.com/assets/img/logo.png)](https://repos.currenciesdirect.com:8443/scm/hyperion/config-server.git)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://repos.currenciesdirect.com:8443/scm/hyperion/config-server.git)

### How to encrypt ?

- On windows

```sh 
curl.exe --data-urlencode ${property-value-to-encrypt} http://${username}:${password}@localhost:8888/encrypt
```
- on linux/mac
```sh 
curl -X POST --data-urlencode ${property-value-to-encrypt} http://${username}:${password}@localhost:8888/encrypt
```

### How to decrypt ?
- On windows

```sh 
curl.exe --data ${encrypted-value} http://${username}:${password}@localhost:8888/decrypt
```
- on linux/mac
```sh 
curl -X POST --data ${encrypted-data} http://${username}:${password}@localhost:8888/decrypt
```

	
	http://localhost:8888/config-client-app/prod
	http://localhost:8888/master/config-client-app.yaml (response is auto converted to yaml even if the orginal file is properties file)
	http://localhost:8888/master/config-client-app-prod.yaml
	
	