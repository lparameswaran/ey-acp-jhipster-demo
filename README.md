# blog
This application was generated using JHipster 5.0.1, you can find documentation and help at [https://www.jhipster.tech/documentation-archive/v5.0.1](https://www.jhipster.tech/documentation-archive/v5.0.1).

## Development tool pre-requisites

1, [Java8][] Install Java 8 from Oracle (your computer probably already has Java 8 installed)
2. [Git][] Install Git https://git-scm.com/
3. [Node.js][] Install Node.js (use an LTS release) http://nodejs.org/
4. [Yarn][] Install Yarn using the Yarn installation instructions Windows: https://yarnpkg.com/lang/en/docs/install/#windows-stable Mac: https://yarnpkg.com/lang/en/docs/install/#mac-stable/
5. [Intellij][] Install IntelliJ IDEA IDE Community Edition https://www.jetbrains.com/idea/download
6. [Maven][] Install Maven from https://www-us.apache.org/dist/maven/maven-3/3.6.0/binaries/apache-maven-3.6.0-bin.zip/
7. [Docker][] Download the Docker Toolbox Windows: https://docs.docker.com/toolbox/toolbox_install_windows/ Mac: https://docs.docker.com/toolbox/toolbox_install_mac/
8. [SonarQube][] Download SonarQube from https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-7.4.zip/


# Step 1: Install required dependent packages
```html
    yarn install
```

# Step 2: In another terminal window, run the client side
```html
    yarn 
    yarn webpack:build
```

# Step 3: In One terminal window, run the server side
```html
    ./mvnw
```

# Step 4: Run the app
```html
    Navigate to [http://localhost:8080](http://localhost:8080) in your browser.
```


# Step 5: Server side Unit Testing
```html
To launch your application's tests, run:
    ./mvnw clean test
```

# Step 6: Client side Unit Testing
```html
Unit tests are run by [Jest][] and written with [Jasmine][]. They're located in [src/test/javascript/](src/test/javascript/) and can be run with:
    yarn test
```

# Step 7: UI End to end Testing
```html
UI end-to-end tests are powered by [Protractor][], which is built on top of WebDriverJS. They're located in [src/test/javascript/e2e](src/test/javascript/e2e)
and can be run by starting server side Spring Boot in one terminal 
    ./mvnw spring-boot:run 
and running the client tests in a second terminal 
    yarn run e2e
```

# Step 8: Continuous Integration

8a. Configure sonar installation -- see SonarQube.md for instructions
8b. Run `jhipster ci-cd` (Note: jhipster supports multiple tools for CI-CD -- for now, choose the options below 
    (Consult the [Setting up Continuous Integration][https://www.jhipster.tech/documentation-archive/v5.0.1/setting-up-ci/] page for more information).
Jenkins pipeline
Analyze code with sonar
http://localhost:9011 as sonar server
8c. Run the jenkins pipeline docker
`docker-compose -f src/main/docker/jenkins.yml up -d`




# [Appendix] 
1. Building for production

To optimize the blog application for production, run:
```html
To concatenate and minify the client CSS and JavaScript files, run the following command. It will also modify `index.html` so it references these new files.
    ./mvnw -Pprod clean package
```
```html
To ensure everything worked, run:
    java -jar target/*.war
```

2. Dockerize

## Using Docker to simplify development (optional)

You can use Docker to improve your JHipster development experience. A number of docker-compose configuration are available in the [src/main/docker](src/main/docker) folder to launch required third party services.

For example, to start a postgresql database in a docker container, run:

    docker-compose -f src/main/docker/postgresql.yml up -d

To stop it and remove the container, run:

    docker-compose -f src/main/docker/postgresql.yml down

You can also fully dockerize your application and all the services that it depends on.
To achieve this, first build a docker image of your app by running:

    ./mvnw verify -Pprod dockerfile:build dockerfile:tag@version dockerfile:tag@commit

Then run:

    docker-compose -f src/main/docker/app.yml up -d
