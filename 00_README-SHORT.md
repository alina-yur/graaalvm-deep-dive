# GraalVM Deep Dive

* GraalVM overview 🐰
* Migrating to GraalVM 🤖
  * 👩‍💻 use Native Build Tools 🛠️
  * 👩‍💻 basic performance measurements with `time` 📈
* Using libraries 📚
  * A library might be designed to be Native-Image friendly out of the box;
  * A library might add config files to its source code;
  * Library configuration can be provided via GraalVM Reachability Metadata Repository ← Use Native Build Tools!
  * 👩‍💻 You can programmatically generate configuration via framework annotations, such as `@ReflectiveAccess`;
  * You can use Native Image's Tracing Agent;
  * You can provide configuration manually via json.
* Peak performance optimizations 🚀
  * 👩‍💻 PGO
    * ML-enabled PGO
  * G1 GC
  * `-march=native`
* Deployment 📦
  * 👩‍💻 Packaging and linking options
  * Linking options: dynamic, mostly static, static
  * CI/CD, GitHub Actions
* Security 🛡️
  *  Security by design
  * 👩‍💻 Vulnerability Scanning
    * `grype`: `native-image-inspect --sbom ./target/demo-sbom | grype -v`
    * `native-image-inspect --sbom ./target/demo-sbom>output.json`
  * 👩‍💻 SBOM support
  * GitHub Action
* Monitoring 📈
  * 👩‍💻 Micrometer
    * (Tempo -> service graph)
  * 👩‍💻 `jvmstat`
  * JFR, JMX, `jcmd`
  * `perf stat <process>`
* In the lab 👩‍🔬
  * Native Image Layers
  * [Project Crema](https://github.com/orgs/oracle/projects/6?pane=issue&itemId=113766307&issue=oracle%7Cgraal%7C11327)
  * [`-H:Preserve=all`](https://github.com/oracle/graal/pull/10180)
  * Embedding Python (Pygal charts)
  * Wasm backend for Native Image