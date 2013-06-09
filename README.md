ICGC DCC - Parent POM
=================
The parent Maven POM for ICGC DCC.

What is it?
-----------
The DCC parent POM provides default configuration for Maven builds.
 
* Recommended/Default versions for the most commonly used Maven plugins
* Manifest configuration for the jar and assembly plugins
* Profiles for generating source jars, and enforcing a minimum versions of 
  Java and Maven
* Distribution Management and other configuration for deploying

How to use it?
--------------
Start out by adding the parent configuration to your pom.

    <parent>
      <groupId>org.icgc.dcc</groupId>
      <artifactId>dcc-parent</artifactId>
      <version>1</version>
    </parent>

The pom includes properties which allow various build configuration to be 
customized.  For example, to override the default version of the
maven-compiler-plugin, just set a property.

    <properties>
      <version.compiler.plugin>2.3</version.compiler.plugin>
    </properties>

Or override the default Java compiler source and target level used in the build.
Note the default level is 1.6.

    <properties>
      <maven.compiler.target>1.6</maven.compiler.target>
      <maven.compiler.source>1.6</maven.compiler.source>
    </properties>

The minimum version of Java or Maven required to run a build can also be set via
properties.

    <properties>
      <maven.min.version>3.0.3</maven.min.version>
      <jdk.min.version>1.6</jdk.min.version>
    </properties>

For the full list of properties, refer to the POM itself.

