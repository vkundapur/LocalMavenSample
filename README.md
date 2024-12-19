### How to publish the aar from the library to local mvn repo

Inside the Library project folder run the following command

```
./gradlew clean publishReleasePublicationToMavenRepository
```

Include the path to the local maven repo like so
```
maven { url = uri(File(System.getProperty("user.home"), ".m2/repository")) }
```

include the library as a dependency
```
implementation("com.vivekrk:greetingslibrary:1.0")
```

Use the library class inside your project
