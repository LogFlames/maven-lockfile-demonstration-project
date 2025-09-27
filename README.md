# Demonstration project for Maven lockfiles

## Generate lockfile
```bash
mvn io.github.chains-project:maven-lockfile:5.7.1:generate -DchecksumMode=local -DincludeMavenPlugins=true
```

## Freeze lockfile
```bash
mvn io.github.chains-project:maven-lockfile:5.7.1:freeze
```

## Validate lockfile
```bash
mvn io.github.chains-project:maven-lockfile:5.7.1:validate
```
