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


# [Step 1] Install required dependent packages
```html
<code>
    yarn install
</code>
```

# [Step 2] In One terminal window, run the server side
```html
<code>
    ./mvnw
</code>
```
# [Step 3] In another terminal window, run the client side
```html
<code>
    yarn start
</code>
```
# [Step 4] Building for production

To optimize the blog application for production, run:
```html
To concatenate and minify the client CSS and JavaScript files, run the following command. It will also modify `index.html` so it references these new files.
<code>
    ./mvnw -Pprod clean package
</code>
To ensure everything worked, run:
<code>
    java -jar target/*.war
</code>
```

# [Step 5] Run the app
```html
<code>
    Navigate to [http://localhost:8080](http://localhost:8080) in your browser.
</code>
```


# [Step 6] Server side Unit Testing
```html
To launch your application's tests, run:
<code>
    ./mvnw clean test
</code>
```

# [Step 7] Client side Unit Testing
```html
Unit tests are run by [Jest][] and written with [Jasmine][]. They're located in [src/test/javascript/](src/test/javascript/) and can be run with:
<code>
    yarn test
</code>
```

# [Step 8] UI End to end Testing
```html
UI end-to-end tests are powered by [Protractor][], which is built on top of WebDriverJS. They're located in [src/test/javascript/e2e](src/test/javascript/e2e)
and can be run by starting server side Spring Boot in one terminal 
<code>
    ./mvnw spring-boot:run 
</code>
and running the client tests in a second terminal 
<code>
    yarn run e2e
</code>
```

# Step 9: Continuous Integration
To configure CI for your project, run the ci-cd sub-generator (`jhipster ci-cd`), this will let you generate configuration files for a number of Continuous Integration systems. Consult the [Setting up Continuous Integration][] page for more information.



# [Appendix] Dockerize

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

For more information refer to [Using Docker and Docker-Compose][], this page also contains information on the docker-compose sub-generator (`jhipster docker-compose`), which is able to generate docker configurations for one or several JHipster applications.

# Continuous Integration (optional)
To configure CI for your project, run the ci-cd sub-generator (`jhipster ci-cd`), this will let you generate configuration files for a number of Continuous Integration systems. Consult the [Setting up Continuous Integration][] page for more information.

[JHipster Homepage and latest documentation]: https://www.jhipster.tech
[JHipster 5.0.1 archive]: https://www.jhipster.tech/documentation-archive/v5.0.1

[Using JHipster in development]: https://www.jhipster.tech/documentation-archive/v5.0.1/development/
[Using Docker and Docker-Compose]: https://www.jhipster.tech/documentation-archive/v5.0.1/docker-compose
[Using JHipster in production]: https://www.jhipster.tech/documentation-archive/v5.0.1/production/
[Running tests page]: https://www.jhipster.tech/documentation-archive/v5.0.1/running-tests/
[Setting up Continuous Integration]: https://www.jhipster.tech/documentation-archive/v5.0.1/setting-up-ci/

[Gatling]: http://gatling.io/
[Node.js]: https://nodejs.org/
[Yarn]: https://yarnpkg.org/
[Webpack]: https://webpack.github.io/
[Angular CLI]: https://cli.angular.io/
[BrowserSync]: http://www.browsersync.io/
[Jest]: https://facebook.github.io/jest/
[Jasmine]: http://jasmine.github.io/2.0/introduction.html
[Protractor]: https://angular.github.io/protractor/
[Leaflet]: http://leafletjs.com/
[DefinitelyTyped]: http://definitelytyped.org/
