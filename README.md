# Forge Enterprise Sample

[![Build Status](https://travis-ci.com/magnolia-community/forge-enterprise-sample.svg?branch=master)](https://travis-ci.com/magnolia-community/forge-enterprise-sample)

## Nexus authentication

In order to download enterprise dependencies from Magnolia's Nexus, the Travis 
job that builds your module needs to authenticate itself. You must therefore 
provide Travis' Maven the credentials you were given when your Forge project 
was created. This is done with environment variables.

You can either add those in Travis' web interface, or have them in 
`.travis.yml`, like this:

    $ brew install travis
    $ cd my-forge-module
    $ travis encrypt USERNAME=<LDAP_USER> --add
    $ travis encrypt PASSWORD=<LDAP_PASSWORD> --add
    $ travis encrypt MASTPASS=<MAVEN_MASTPASS> --add
