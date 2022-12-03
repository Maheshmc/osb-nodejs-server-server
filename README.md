**Readme for updating server specific code using NodeJs:**

Follow the instructions below to update your server specific code using NodeJs:

1. Log into your Github account and clone the source code from the GitHub repo: osb-nodejs-server.
2. Extract the source files in your local system.
3. With the help of the table below, create your service specific code by updating the file name and function name for each of the tasks that you wish to configure for your service.

**Open Service Broker API Specifications for NodeJs:**

| S.No | Task Name                                                     | File Name                        | Function Name                           |
|------|---------------------------------------------------------------|----------------------------------|-----------------------------------------|
| 1    | Get a Service instance                                        | controllers/ ServiceInstances.js | serviceInstanceGetUsingGET              |
| 2    | Provisioning new service instance                             | controllers/ ServiceInstances.js | serviceInstanceProvisionUsingPUT        |
| 3    | Deprovisioning service instance                               | controllers/ ServiceInstances.js | serviceInstanceDeprovisionUsingDELETE   |
| 4    | Update a service instance                                     | controllers/ ServiceInstances.js | serviceInstanceUpdateUsingPATCH         |
| 5    | Get the latest requested operation state for service instance | controllers/ ServiceInstances.js | serviceInstanceLastOperationGetUsingGET |
| 6    | Get a service binding                                         | controllers/ ServiceBindings.js  | serviceBindingGetUsingGET               |
| 7    | Generate a service binding                                    | controllers/ ServiceBindings.js  | serviceBindingBindingUsingPUT           |
| 8    | Deprovision a service binding                                 | controllers/ ServiceBindings.js  | serviceBindingUnbindingUsingDELETE      |
| 9    | Get the latest requested operation state for service binding  | controllers/ ServiceBindings.js  | serviceBindingLastOperationGetUsingGET  |
| 10   | Get Catalog                                                   | controllers/Catalog.js           | catalogGetUsingGET                      |

4. Commit the code changes and push the changes to the main branch.
5. Open the command line terminal and execute the following command to update the broker image and to deploy your service specific code:

   **python3 application_update.py**

**Note**: Ensure that the environment variables are set in the "env" file. For more information on how to set the environment variables, refer to [Pre-requisites for running the script](https://github.ibm.com/Code-Your-Skills/accelerating-partner-service-onboarding/edit/main/Readme/nodejs-server-readme.md).

Enter the number to select your preferred coding language. You can choose any of the following languages:

* Java-Spring
* Python-flask
* Scala
* Nodejs-server
* Go-server
* Ruby

Once the script starts running, you will get the following output as shown below:

**INFO:Generating the source code for go-server using the swagger code-generator docker run --rm -v /Users/local swaggerapi/swagger-codegen-cli-v3 generate -i https://raw.githubusercontent.com/openservicebrokerapi/servicebroker/master/openapi.yaml -l go-server -o /local/osb-go-server-server INFO:Updating the local repo with readme and dockerfile, push swagger generated code to github repository INFO:add files and commit the changes INFO:Add git remote origin INFO:Completed pushing the code to github repository INFO:Create and deploy app in code engine ./create_codeEngine.sh --apikey mt64-xjeL1on8EkUkA6g68MXYyBGW3TqxugKC84kIl-0 --region us-south --resource_group Default --lang go-server --git_url https://github.com/OSB-Hackathon/osb-go-server-server.git --port_num 8080 https://test-go-server-app.vyy1fq8t3fh.us-south.codeengine.appdomain.cloud https://github.com/OSB-Hackathon/osb-go-server-server.git**

  
The output of this script is an URL for the service broker, along with the CodeEngine URL. If the URL gets loaded successfully in a browser window, it implies that the service broker is generated successfully.

https://test-go-server-app.vyy1fq8t3fh.us-south.codeengine.appdomain.cloud - Sample URL for the service broker.

https://github.com/OSB-Hackathon/osb-go-server-server.git - Sample URL for the Gitrepo, where the code is pushed to.

    
