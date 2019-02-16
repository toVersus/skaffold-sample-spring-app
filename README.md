# skaffold-sample-spring-app

You can deploy this hello world application on your local Kubernetes environment
by using [Jib](https://github.com/GoogleContainerTools/jib) and [Skaffold](https://github.com/GoogleContainerTools/skaffold).

## Requirement

- Docker Desktop for Mac: Version 2.0.0.3
    - Docker Engine: 18.09.2
    - Kubernetes: v1.10.11
- OpenJDK

  ```
  openjdk version "1.8.0_192"
  OpenJDK Runtime Environment (build 1.8.0_192-amazon-corretto-preview2-b12)
  OpenJDK 64-Bit Server VM (build 25.192-b12, mixed mode)
  ```
- Kotlin: 1.2.71
- Spring Boot: 2.1.3.RELEASE
- jib-gradle-plugin: 1.0.0


## Usage

1. Install Skaffold executable from [release page](https://github.com/GoogleContainerTools/skaffold/releases)

2. Run the following command:

    ```bash
    $ skaffold dev
    ```

3. If any code changes are made, Skaffold automatically rebuild the container image by using jib-plugin
and deploy app with LB Service. Then, you just access to http://localhost:8080/greeting/hello?name=foo.
