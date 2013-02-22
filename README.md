<h1>JBoss JavaEE Specs API</h1>
This project provides dependency management for a complete set of required APIs as defined by the Java EE Platform Specifications.

Starting with the community release of <a href="http://community.jboss.org/wiki/AS600FinalReleaseNotes">JBoss Application Server 6.0.0.Final</a>, this project was modified to provide an aggregation of the APIs required as part of the Java EE 6 Platform Specification.  The project originated from the legacy jbossas/projects/specs <a href="http://svn.jboss.org/repos/jbossas/projects/specs/">SVN repository</a> and later <a href="http://community.jboss.org/wiki/JBossJavaEESpecsGitMigration">migrated</a> to <a href="https://github.com/jboss/">github/jboss</a> repository.
The goals initiating this move and restructure were:

<ul>
<li>Maintain a single repository containing the required APIs as defined by the EE Platform Specification</li>
<indent>Having a consistent structure for all the EE APIs make it easier to access, maintain, and consume.</indent>


<li>Individual release cycle per technology component</li>
<indent>Restructuring the project so each API set can be released individually provides greater flexibility and control to the project owners without waiting for the aggregate to be released and integrated.  These API releases can be consumed by your project as a single dependency or as a full set of required APIs via the <a href="http://repository.jboss.org/nexus/content/groups/public/org/jboss/spec/jboss-javaee-6.0/">Java EE</a> and <a href="http://repository.jboss.org/nexus/content/groups/public/org/jboss/spec/jboss-javaee-web-6.0/">Java EE Web</a> BOMs.</indent>

<li>Define a naming scheme to associate the Specification version to the the APIs contained in the JAR and distinguish between that and the release version of the artifact</li>
<indent>
The naming scheme adopted is as follows:
<ul>
<li>groupId:    org.jboss.spec + the package name
<li>artifactId: Technology-api_SpecVersion_spec
<li>version:    release version of the artifact
</ul>
Using the Servlet 2.5 API Specification as an example:
<ul>
<li><code>&lt;groupId&gt;org.jboss.spec.javax.servlet&lt;/groupId&gt;</code>
<li><code>&lt;artifactId&gt;servlet-api_2.5_spec&lt;/artifactId&gt;</code>
<li><code>&lt;version&gt;1.0.0-SNAPSHOT&lt;/version&gt;</code>
</ul>
</indent>
<li>Promote adoption of these spec-versioned APIs in all JBoss projects</li>
<indent>The APIs released from the org.jboss.specs project are certified for compliance to their respective specification.</indent>
</ul>
