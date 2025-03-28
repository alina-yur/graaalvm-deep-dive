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
  * Overview of compiler optimization levels
  * 👩‍💻 PGO
  * ML-enabled PGO
  * G1 GC
  * `-march=native`
  * Memory management (`xmx` settings, object headers)
* Testing 👨‍🔬 // add a demo
* Deployment 📦
  * 👩‍💻 Packaging and linking options
    * JVM | Dynamic | OpenJDK
    * JVM | Dynamic | OpenJDK-jlink
    * Native | Dynamic | Debian
    * Native | Mostly static | Distroless base?
    * Native | Static | From scratch 
    * Native | Static | From scratch | Optimize for size
  * scan the images for vulnerabilities & packages 🛡️
  * Buildpacks
  * GitHub actions
* Security 🛡️
  * 👩‍💻 Security by design
  * 👩‍💻 SBOM support: exposing in Spring Actuator, `grype` exporting sbom!
  * Vulnerability Scanning
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
