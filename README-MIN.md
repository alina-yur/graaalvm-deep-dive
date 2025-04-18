# GraalVM Deep Dive

* GraalVM overview 🐰
* Migrating a Spring app to GraalVM 🤖
  * 👩‍💻 use Native Build Tools 🛠️
  * 👩‍💻 basic performance measurements with `time` 📈
* Using libraries 📚
  * A library might be designed to be Native-Image friendly out of the box;
  * A library might add config files to its source code;
  * Library configuration can be provided via GraalVM Reachability Metadata Repository;
  * 👩‍💻 You can programmatically generate configuration via framework annotations, such as `Reflective`;
  * You can use Native Image's Tracing Agent;
  * You can provide configuration manually via json.
* Peak performance optimizations 🚀
  * 👩‍💻 PGO
    * ML-enabled PGO
  * G1 GC
  * `-march=native`
* Developing & testing 👨‍🔬
* Deployment 📦
  * 👩‍💻 Packaging and linking options
  * Buildpacks
  * GitHub actions
* Security 🛡️
  *  Security by design
  * 👩‍💻 Vulnerability Scanning
    * `grype`: `native-image-inspect --sbom ./target/demo-sbom | grype -v`
    * `native-image-inspect --sbom ./target/demo-sbom>output.json`
  * 👩‍💻 SBOM support: exposing in Spring Actuator
  * GitHub Action
* Monitoring 📈
  * 👩‍💻 Micrometer
    * (Tempo -> service graph)
  * 👩‍💻 `jvmstat`
  * JFR, JMX, `jcmd`
  * `perf stat <process>`
* In the lab 👩‍🔬
  * Native Image Layers
  * Project Crema
  * [`-H:Preserve=all`](https://github.com/oracle/graal/pull/10180)
  * Embedding Python (Pygal Spring Boot)
  * Wasm backend for Native Image