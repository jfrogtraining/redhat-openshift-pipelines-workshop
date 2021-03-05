﻿---
title: "Install and Configure the JFrog CLI"
chapter: false
weight: 433
pre: "<b>4.3.3 </b>"
---

JFrog CLI is a client that provides a simple CLI interface that automates the management of JFrog products. JFrog CLI works with JFrog Artifactory, JFrog Mission Control, JFrog Bintray and JFrog Xray (through their respective [REST APIs](https://www.jfrog.com/confluence/display/JFROG/REST+API)) making your scripts more efficient and reliable. You can use the JFrog CLI to assist in your builds, create artifacts, promote artifacts, trigger security scans and much more. It is powerful to that you can use in your CI/CD process and general automation. You can learn more [here](https://www.jfrog.com/confluence/display/CLI/JFrog+CLI). 

1. In your Red Hat Openshift Cloud Shell, run the following shell commands to install the JFrog CLI.

```
curl -fL https://getcli.jfrog.io | sh
mkdir ~/bin
mv jfrog ~/bin/
```

![JFrog CLI Install](/images/jfrog-cli-install.png)

2. Execute the following to test the JFrog CLI and check the version.

``
jfrog --version
``

3. Set the following environment variables. Substitute your JFrog Platform credentials (_username_ and _API key_).

``
export JFROG_USER=<username/email>
``

``
export JFROG_APIKEY=<api key>
``

4. Next, we will configure the JFrog CLI to use our JFrog Platform credentials (_username_ and _API key_). Execute the following command. Substitute your JFrog Platform credentials (_username_ and _API key_).

``
jfrog rt config --user $JFROG_USER --apikey $JFROG_APIKEY
``

5. When prompted, enter a unique _Artifactory server ID_ such as your JFrog Platform server name. Remember this ID.
6. Enter the URL for the JFrog Artifactory server which has the _artifactory_ path.
7. Then accept the remaining default values. If you make a mistake, you can rerun the command again.

![JFrog CLI Config](/images/jfrog-cli-config.png)

8. And let's set an environment variable for our _Artifactory server ID_.

``
export JFROG_SERVER_ID=<server ID>
``

9. Execute the following to list your Artifactory servers that are configured in the JFrog CLI.

``
jfrog rt config show
``

10. Execute the following command to check connectivity to the server. You should get an _OK_ response.

``
jfrog rt ping
``
