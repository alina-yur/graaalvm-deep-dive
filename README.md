# GraalVM Deep Dive

* GraalVM overview 🐰
* Migrating a Spring app to GraalVM, running on the JVM vs native 🤖
  * 👩‍💻 use Native Build Tools 🛠️
  * 👩‍💻 basic performance measurements with `time` 📈
* Using libraries 📚
  * A library might be designed to be Native-Image friendly out of the box;
  * A library might add config files to its source code;
  * Library configuration can be provided via GraalVM Reachability Metadata Repository;
  * 👩‍💻 You can programmatically generate configuration via framework annotations, such as `Reflective`;
  * You can use Native Image's Tracing Agent;
  * You can provide configuration manually via json.
* Performance optimizations 🚀
  * [Overview of compiler optimization levels](https://github.com/alina-yur/native-spring-boot?tab=readme-ov-file#optimization-levels-in-native-image)
  * 👩‍💻 PGO
    * ML-enabled PGO
  * G1 GC
  * `-march=native`
  * Memory management (`xmx`, object headers)
* Testing 👨‍🔬 <!-- mvn -Pnative test -->
* Deployment 📦
  * 👩‍💻 Packaging and linking options
    * JVM | Dynamic | Temurin
    * JVM | Dynamic | OpenJDK-jlink
    * Native | Dynamic | Java-base-debian
    * Native | Mostly static | Distroless
    * Native | Static | From scratch 
    * Native | Static | From scratch | Optimize for size
  * scan the images for vulnerabilities & packages 🛡️
  * Buildpacks
  * GitHub actions
* Security 🛡️
  *  Security by design
  * 👩‍💻 Vulnerability Scanning: `grype`
  * 👩‍💻 SBOM support: exposing in Spring Actuator
  * GitHub Action
* Monitoring 📈
  * 👩‍💻 Micrometer
  * 👩‍💻 `jvmstat` <!-- visualvm --jdkhome /Users/ayurenko/.sdkman/candidates/java/23-graal --> 
  * JFR, JMX, `jcmd`
  * `perf stat <process>` (event)?
* Tooling 🔮
  * 👩‍💻 Build reports
* In the lab 👩‍🔬
    * _"Why do it? Because we can"_
    * _"We do these things not because they are easy, but because we thought they were going to be easy"_
  * Llama3.java
  * Layers // add img
  * Crema
  * [`-H:Preserve=all`](https://github.com/oracle/graal/pull/10180)
  * Wasm backend // try a demo - helloworld?
  * Embedding Python (Pygal Spring Boot)
