h1. What is it?
This is bunch of Eclipse Virgo plans to enable a fully-fledged osgiliath ESB project

h2. How to use?

First you have to configure your maven settings.xml to mirror the osgiliath nexus (http://bugzilla.osgiliath.net/projects/osgiliath-superpom/wiki).

In a second time, configure in this file a maven active profile with the property virgo.path pointing on your root virgo installation (3.6.0.RELEASE at the time I'm writing). 
Add entry javax.persistence.metamodel to the spring orm MANIFEST (on the repository/ext folder).

Finally just run mvn clean install and launch Virgo!

h2. Architecture

You can clone the git project at http://subversion.osgiliath.net/git-private/karaf.features.git

It's composed of a parent pom and multiples modules (plans):

* derby for the database
* jpa for persistence
* validation for hibernate validation (with an osgi service)
* security for spring security
* messaging for jms and websocket (jms connection is exported)
