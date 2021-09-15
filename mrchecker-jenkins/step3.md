
### Jenkinsfile
The next file we will tak a look is Jenkinsfile. If you are not planing use with Jenkins you can skip this.

Let's open `my-new-fantastic-project/Jenkinsfile`{{open}}

### Job parameters
In section parameters you will find a job parameters which allow users to choose on which grid tests should execute, which group should be executed and on which browser.

### Stages

#### Preparation
In preparation stage we are runing `mvn clean` command to clean `target` directory at the very begining.

#### Test
In test stage we have 2 substages Selenium where we are running selenium testcases.
There is also a WebAPI substage to indicate that diferent test types might use diferent stages to indicate the progress.

#### Poststep
The post step contains commented out mailing procedure. To make it work you need to accept some unsafe (from jenkins point of view) methods. It's also an indication you can send the mail after each job to person who started it. If there are any other actions to be taken at the end of every job thats the correct place.

### Secretdata
The Jenkins will tell you it's missing the secretdata file. You can put it in `Manage Jenkins` -> `Managed Files`
And then add it with the following block
```groovy
configFileProvider([configFile(fileId: 'secretData', targetLocation: 'secretdata.csv', variable: 'variable')]) {
    // some other code using secretdata
}

```

