# Demonstration of Maven Lockfile

## 1. Generate lockfile
```bash
mvn io.github.chains-project:maven-lockfile:5.7.1:generate -DchecksumMode=local -DincludeMavenPlugins=true
```

## 2. Freeze lockfile
```bash
mvn io.github.chains-project:maven-lockfile:5.7.1:freeze
```

Check difference between original `pom.xml` and frozen `pom.lockfile.xml`.

Build project using the frozen pom
```bash
mvn -f pom.lockfile.xml clean verify
```

## 3. Validate lockfile
```bash
mvn io.github.chains-project:maven-lockfile:5.7.1:validate
```

Edit pom, check validation fails.

Edit dependency, check validation fails. 
