[![License](https://img.shields.io/badge/license-Apache%20License%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Java](https://img.shields.io/badge/java-17%2B-blue)](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
[![GitHub CI](https://github.com/gbevin/rife2-hello/actions/workflows/gradle.yml/badge.svg)](https://github.com/gbevin/rife2-hello/actions/workflows/gradle.yml)

# RIFE2 bootstrap project structure

This project helps you to get started with a RIFE2 web application and Gradle.

You'll find all the pieces that are explained in the first sections of
[the documentation](https://github.com/gbevin/rife2/wiki) neatly contained
in this one project.

It's ready to run, package and deploy ... and for you to have fun developing
in a very iterative, intuitive and rewarding way.

For all things RIFE2, head on to the project website:
[https://rife2.com](https://rife2.com)

## Run the tests

```bash
./gradlew clean test
```

## Running the server

```bash
./gradlew clean run
```

Go to:

[http://localhost:8080/](http://localhost:8080/)


## Deploying the app

```bash
./gradlew clean war
```

The resulting archive will be in:
`war/build/libs`

If you use any of the byte-code instrumented features , like continuations,
metadata merging or lazy-loaded database entities, you'll need to launch your
servlet container with the `-javaagent:[path-to]/rife2-*-agent.jar` argument.
Exactly how is dependent on each servlet container.

## Making an UberJar


```bash
./gradlew clean uberJar
```

Then run it with:

```bash
java -jar app/build/libs/hello-uber-1.0.jar
```

If you use any of the byte-code instrumented features, you'll need to also tell
`java` to use the RIFE2 agent.

For example:

```bash
java -javaagent:[path-to]/rife2-*-agent.jar -jar app/build/libs/hello-uber-1.0.jar
```

## Get in touch

Thanks for using RIFE2!

If you have any questions, suggestions, ideas or just want to chat, feel free
to post on the [forums](https://github.com/gbevin/rife2/discussions), to join
me on [Discord](https://discord.gg/DZRYPtkb6J) or to connect with me on
[Mastodon](https://uwyn.net/@gbevin).


**Read more in the [full documentation](https://github.com/gbevin/rife2/wiki)
and  [RIFE2 Javadocs](https://gbevin.github.io/rife2/).**
