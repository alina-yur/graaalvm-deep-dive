# GraalVM Deep Dive

* GraalVM overview 🐰
* Migrating a Spring app to GraalVM, running on the JVM vs native 🤖
  * use Native Build Tools 🛠️
  * basic performance measurements with `time` 📈
* Using libraries 📚
  * A library might be designed to be Native-Image friendly out of the box;
  * A library might add config files to its source code;
  * Library configuration can be provided via GraalVM Reachability Metadata Repository;
  * You can programatically generate configuration via framework annotations, such as `Reflective`;
  * You can use Native Image's Tracing Agent;
  * You can provide configuration manually via json.
 * Performance optimizations 🚀
    * Overview of compiler optimization levels
    * PGO
    * ML-enabled PGO
    * G1 GC
    * `-march=native`
 * Deployment 📦
    * Packaging and linking options
    * Buildpacks
    * GitHub actions  
 * Monitor 📈
    * Micrometer
    * `jvmstat`
    * JFR, JMX, `jcmd`
* Security 🛡️
    * Security by design
    * SBOM support 
