# Forge Enterprise Sample

[![Build Status](https://travis-ci.com/magnolia-community/forge-enterprise-sample.svg?branch=master)](https://travis-ci.com/magnolia-community/forge-enterprise-sample)

This page describes required steps in case you want to do a Forge module that 
uses Magnolia Enterprise dependencies. Please make sure to read [the Forge 
Community sample][ce-readme] first.

## Nexus authentication

In order to download enterprise dependencies from Magnolia's Nexus, the Travis 
job that builds your module needs to authenticate itself. You must therefore 
provide Travis' Maven your enterprise credentials. This is done with 
environment variables.

You can either add those in Travis' web interface, or have them in 
`.travis.yml`, like this:

    $ brew install travis
    $ cd my-forge-module
    $ travis encrypt USERNAME=<LDAP_USER> --add
    $ travis encrypt PASSWORD=<LDAP_PASSWORD> --add
    $ travis encrypt MASTPASS=<MAVEN_MASTPASS> --add

## Deployment

Please include release coordinates in your README so that your module can be 
used by others. The [README blueprint][blueprint] will provide you with a 
template that's easy to adapt.

## Help

Whether you need help, would like to share your work, or simply get in touch 
with the community, you can join the [Magnolia User Google 
Group][google-group].

[blueprint]:https://github.com/magnolia-community/forge-community-sample/blob/master/README-blueprint.md
[magnolia-community]:https://github.com/magnolia-community
[ce-readme]:https://github.com/magnolia-community/forge-community-sample
