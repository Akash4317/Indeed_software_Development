## Software Development

#### Q1. Threads allow a developer to.
- [ ] have tasks to completed in the correct order
- [x] perform tasks in parallel
- [ ] deploy only certain modules of an application
- [ ] reduce the resources needed for an application
- [ ] build a less complex application

⭐ Threads enable concurrent execution, improving performance by running multiple tasks simultaneously, utilizing multiple cores efficiently.

##

#### Q2. Which process requires automated builds and testing to verify software during development?

- [x] Continuous integration
- [ ] System integration
- [ ] Agile methodology
- [ ] Deployment integration
- [ ] Integration tests

➡️ Continuous integration refers to the build and unit testing stages of the software release process. Every revision that is committed triggers an automated build and test. With continuous delivery, code changes are automatically built, tested, and prepared for a release to production.

##

#### Q.3 one strategy to keep file writes atomic is to 

- [ ] configure appropriate  system settings such as KEEP_FILE_WRITE_ATOMIC
- [ ] write to a temporary  file, then rename the temporary file to the  original file via the system setting
- [ ] use a write-through cache to store the file until it can be written automatically
- [ ] write a file once read it back  and then rewrite it 
- [ ] concatenate the new file to the existing file 


##

#### Q4. You have two microservices that need to communicate with each other without holding up a thread on either end. One service will receive an ID and return a message once the job is complete. Which communication framework should be used?

- [ ] Create a third service to handle the interaction between the services
- [ ] Have a shared database that allows both applications to read and write to the tables to share the data instead of having to communicate
- [x] Use a RESTful architecture for both, send the ID through a POST, and ping the service with a GET until a response is available
- [ ] Use asynchronous messaging to send and receive messages between each microservice
- [ ] Abandon the microservice architecture so no interaction is needed


##

#### Q.5 You need to built  

