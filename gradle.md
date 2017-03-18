# Good tuts
https://spring.io/guides/gs/gradle/

http://tutorials.jenkov.com/gradle/gradle-tutorial.html

# Run build script
```
gradle
```

# Run a task
```
gradle task_name
```

# Run multple tasks
```
gradle task1 task2
```

# Exclude task (if one task depends on another)
```
gradle build -x test
```

# Quite mode (no status messages in console)
```
gradle -q task_name
```

# Listings
## Tasks
```
gradle tasks
gradle tasks --all
```
## Subprojects
```
gradle projects
gradle projects --all
```

# Specifying build script
```
gradle -b subproject-dir/build.gradle build
```

# Specifying project to build
```
gradle -p subproject-dir build
```


