# spring-cloud-config-server


publish various endpoint for accessing the properties. Also supports encryption as rest/transmit
This example do not cover the encryption.


Expose the properties from git repository. Retrive the properties based on application name, profile, label(branch) default branch is master if not specified

${application-name}-${profile-set-in-properties}-${label/branch}
for eg. http://localhost:8888/config-client-app/default

	application name config-client-app
	profile: default
	
	this will resolve to config-client-app.propeties and global properties defined in application.properties
	
	
	http://localhost:8888/config-client-app/prod
	http://localhost:8888/master/config-client-app.yaml (response is auto converted to yaml even if the orginal file is properties file)
	http://localhost:8888/master/config-client-app-prod.yaml
	
	