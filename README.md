<h1>JBoss JavaEE Specs API</h1>
This project provides dependency management for a complete set of required APIs as defined by the Java EE Platform Specifications.

This project, which originated from the legacy <a href="http://svn.jboss.org/repos/jbossas/projects/specs/">jbossas/projects/specs SVN repository</a>, was enhanced to produce an aggregation of the APIs required by the Java EE Platform Specification.  Further changes included <a href="http://community.jboss.org/wiki/JBossJavaEESpecsGitMigration">migration</a> to a <a href="https://github.com/jboss/">github/jboss</a> repository.  The goals initiating this move and restructure were:

<ul>
<li>Maintain a single repository containing the required APIs as defined by the EE Platform Specification</li>
<indent>Having a consistent structure for all the EE APIs make it easier to access, maintain, and consume.</indent>

<li>Individual release cycle per technology component</li>
<indent>Restructuring the project so each API set can be released individually provides greater flexibility and control to the project owners without waiting for the aggregate to be released and integrated.  These API releases can be consumed by your project as a single dependency or as a fully defined set of required APIs for the profile.

<li>Define a naming scheme to associate the Specification version to the the APIs contained in the JAR and distinguish between that and the release version of the artifact</li>
<indent>
The naming scheme adopted is as follows:
<ul>
<li>groupId:    org.jboss.spec + the package name
<li>artifactId: Technology-api_SpecVersion_spec
<li>version:    release version of the artifact
</ul>
</indent>
<li>Promote adoption of these spec-versioned APIs in all JBoss projects</li>
<indent>The APIs released from the org.jboss.specs project are certified for compliance to their respective specification.</indent>
</ul>

<h2>Java EE Full Profile APIs</h2>
If you require the full set of required technology APIs defined by the Java EE specification, add the following to your project pom.
<ul>
<li><code>&lt;groupId&gt;org.jboss.spec&lt;/groupId&gt;</code>
<li><code>&lt;artifactId&gt;jboss-javaee-7.0&lt;/artifactId&gt;</code>
<li><code>&lt;version&gt;<a href="https://repository.jboss.org/nexus/content/groups/public/org/jboss/spec/jboss-javaee-7.0/1.0.0.CR1">1.0.0.CR1</a>&lt;/version&gt;</code>
</ul>

<h2>Java EE Web Profile APIs</h2>
If you are developing web applications and depend only on technologies that comprise the Java EE Web Profile specification, you can opt to use the web profile pom.
<ul>
<li><code>&lt;groupId&gt;org.jboss.spec&lt;/groupId&gt;</code>
<li><code>&lt;artifactId&gt;jboss-javaee-web-7.0&lt;/artifactId&gt;</code>
<li><code>&lt;version&gt;<a href="https://repository.jboss.org/nexus/content/groups/public/org/jboss/spec/jboss-javaee-web-7.0/1.0.0.CR1">1.0.0.CR1</a>&lt;/version&gt;</code>
</ul>

<h2>Java EE API UberJar</h2>
Else, if you prefer a jar containing the EE API classes, that is also made available per a previous <a href="https://issues.jboss.org/browse/JBEE-73">feature request</a>.
<ul>
<li><code>&lt;groupId&gt;org.jboss.spec&lt;/groupId&gt;</code>
<li><code>&lt;artifactId&gt;jboss-javaee-7.0-all&lt;/artifactId&gt;</code>
<li><code>&lt;version&gt;<a href="https://repository.jboss.org/nexus/content/groups/public/org/jboss/spec/jboss-javaee-all-7.0/1.0.0.CR1">1.0.0.CR1</a>&lt;/version&gt;</code>
</ul>


These examples show the group:artifactId for use with Java EE 7.    <a href="https://repository.jboss.org/nexus/content/groups/public/org/jboss/spec/">Releases</a> are available for Java EE 6 also.
