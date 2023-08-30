# Example of Keycloak deploy on Platform.sh

This is an example of the deploy of a Keycloak instance on Platform.sh.
It includes the reading of Platform.sh variables for Keycloak self configuration as well as a split hostname for the application admin.

## Features
* Java 17
* MariaDB 10.4

## Customizations

The .environment file is read by Platform.sh to export the needed variables for Keycloak configuration.
Those keys are listed in Keycloak documentation for additional changes and configuration: [Documentation](https://www.keycloak.org/server/all-config)
As Keycloak is provided as an archive, the $VERSION variable in the .platform.app.yaml manages the version to be download and installed. The current setups verifies is the archive is already in cache to avoid downloading it at each build.
