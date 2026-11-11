# NextWork Java web learning sample

A guided Maven WAR sample containing a JSP and servlet descriptor. No database, API, authentication or AWS provisioning code is supplied.

- [Technical architecture, diagrams and maintenance](docs/ARCHITECTURE.md)
- [Portable build](pom.xml)
- [Build-only CodeBuild configuration](buildspec.yml)

## Build

With JDK 17+ and Maven 3.9.x:

```bash
mvn --batch-mode --no-transfer-progress clean verify
jar tf target/nextwork-web-project.war
```

The resulting WAR requires a separately configured compatible JSP/servlet container. Packaging does not prove deployment. Default builds require no AWS account. The optional `settings.xml` private mirror requires your own `CODEARTIFACT_MAVEN_URL` and `CODEARTIFACT_AUTH_TOKEN`; never commit token values.
