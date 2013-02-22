JBoss JavaEE Specs API project provides dependency management encompassing a complete set of required APIs as defined by the Java EE Platform Specifications.

Starting with the community release of <a href="http://community.jboss.org/wiki/AS600FinalReleaseNotes">JBoss Application Server 6.0.0.Final</a>, this project was modified to provide an aggregation of the APIs required as part of the Java EE 6 Platform Specification.  The project was originated from the legacy <a href="http://svn.jboss.org/repos/jbossas/projects/specs/">jbossas/projects/specs SVN repository</a> and later <a href="http://community.jboss.org/wiki/JBossJavaEESpecsGitMigration">migrated to git</a>.
The goals initiating this move and restructure were:

<ul>
<li>Maintain a single repository containing the required APIs as defined by the EE Platform Specification.
Having a consistent structure for all the EE APIs will to make it easier to access, maintain, and consume.


<li>Individual release cycle per technology component
Restructuring the project so each API set can be released individually provides greater flexibility and control to the project owners without waiting
for the aggregate to be released and integrated.
These API releases can be consumed by your project as a single dependency or as a full set of required APIs via the Java EE and Java EE Web BOMs.


<li>Define a naming scheme to associate the Specification version to the the APIs contained in the JAR and distinguish between that and the release version of the artifact.
The naming scheme adopted is as follows:
<ul>
<li><bold>groupId:</bold>  org.jboss.spec + the package name
<li><bold>artifactId:</bold> Technology-api_SpecVersion_spec
<li><bold>version:</bold>  release version of the artifact
</ul>
Using the Servlet 2.5 API Specification as an example:
<ul>
<li><code>&lt;groupId&gt;org.jboss.spec.javax.servlet&lt;/groupId&gt;</code>
<li><code>&lt;artifactId&gt;servlet-api_2.5_spec&lt;/artifactId&gt;</code>
<li><code>&lt;version&gt;1.0.0-SNAPSHOT&lt;/version&gt;</code>
</ul>
<li>Promote adoption of these spec-versioned APIs for consistency in all JBoss-released projects.  
The APIs released from the org.jboss.specs project are certified for compliance to their respective specification.
</ul>
