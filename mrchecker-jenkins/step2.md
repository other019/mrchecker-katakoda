Ok we have the template extracted and set up. Now its time to customize it a bit.

## Task

Enter the folder my-new-fantastic-project `cd ./my-new-fantastic-project && ls`{{execute}}.
We will go through few important files

### pom.xml
Open file `pom.xml`{{open}}

In line 6 **<artifactId> tag** you need to edit your artifact id. Change it to something which describe your project like `ProjectLambdaE2E`.
In line 7 **<groupId> tag** you might want to edit group id for something whit is in line with the patern `<top-level-domain>.<company>.<project>` so for example `com.codefact.projectlambda`.
In line 8 **<version> tag** you might change this version so when runing the tests it will be shown with diferent one. For now `0.0.1-SNAPSHOT` seems quite ok.

In line 16 **<developers> tag** you might want to enter developers of the project so everybody will know who the project belongs to.

### environment.csv
Open file `my-new-fantastic-project/src/resources/enviroments/environments.csv`{{open}}.
This is a csv file with environment variables such as environmnet URL. On the columns are different environments such as `DEV` `QA` `PROD`. As `DEV` is the default one it would be good to change the url to the one pointing to your environment.

