```
cf login -a api.run.pivotal.io #(enter your PCF login info)
 
cf push #send the petclinic app to PCF
cf create-user-provided-service contrast-security-service -p "teamserver_url, username, api_key, service_key"
#(new prompts will ask you for the TeamServer URL, username, api_key, service_key.  Make sure username and service key are for the same username. i.e. rali.kettani@contrastsecurity.com and api_key is available in profile section)
cf bind-service contrast-pcf-petclinic contrast-security-service
cf restage contrast-pcf-petclinic
```