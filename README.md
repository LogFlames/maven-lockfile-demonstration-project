# Demonstration of Maven Lockfile

## 1. Generate lockfile
```bash
mvn io.github.chains-project:maven-lockfile:5.7.1:generate -DchecksumMode=local -DincludeMavenPlugins=true
```

## 2. Validate lockfile
```bash
mvn io.github.chains-project:maven-lockfile:5.7.1:validate
```

Edit pom, check validation fails.

Edit dependency, check validation fails. 

## 3. Rebuild from lockfile

### 3.1. Freeze lockfile
```bash
mvn io.github.chains-project:maven-lockfile:5.7.1:freeze
```

Check difference between original `pom.xml` and frozen `pom.lockfile.xml`.

### 3.2. Rebuild from frozen pom
Build project using the frozen pom
```bash
mvn -f pom.lockfile.xml clean verify
```
