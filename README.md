# eclipse-testing-cross-rcptt
This is an example on how execute [RcpTT][2] test from Nexus repository on a custom eclipse product

It will use 2 DSML [Papyrus][1] based: [SysML 1.4][3] and [Papyrus-RT][4].
It will create a product containing all the features (using [Maven][5]-[Tycho][6]) 
then execute the RcpTT tests (present in Eclipse-Papyrus-Nexus and Eclipse-Papyrus-RT-Nexus)

# Status
License [![License](https://img.shields.io/badge/license-EPL-blue.svg)](https://www.eclipse.org/legal/epl-v10.html)



## How to build & run tests
```
mvn clean install
```

Optionnal to avoid some tycho mixture
```
 -Dtycho.localArtifacts=ignore 
```
or
```
-Dtycho.disableP2Mirrors=true
```
## Project structure:
 - com.github.bmaggi.eclipse.testing.product : package SysML 1.4 and Papyrus-Rt in an eclipse product
 - com.github.bmaggi.eclipse.testing.rcptt : module that execute SysML 1.4 and Papyrus-Rt RcPTT tests  
 - com.github.bmaggi.eclipse.testing.targetplatform.mars: eclipse targetplatform used to construct the product
 

 
[1]: https://eclipse.org/papyrus/
[2]: https://eclipse.org/rcptt/
[3]: https://git.eclipse.org/c/papyrus/org.eclipse.papyrus-sysml.git/
[4]: https://www.eclipse.org/papyrus-rt/
[5]: https://maven.apache.org/
[6]: https://eclipse.org/tycho/
