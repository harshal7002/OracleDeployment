# OracleDeployment


<settings>
  <servers>
    <server>
      <id>nexus-repo</id>
      <username>${NEXUS_USERNAME}</username>
      <password>${NEXUS_PASSWORD}</password>
    </server>
  </servers>
</settings>


mvn deploy:deploy-file \
  -DgroupId=com.yourcompany.project \
  -DartifactId=your-app \
  -Dversion=1.0.0 \
  -Dpackaging=war \
  -Dfile=target/your-app.war \
  -DgeneratePom=true \
  -DrepositoryId=nexus-repo \
  -Durl=http://<nexus-host>:8081/repository/maven-releases/ 
