# ONNXRuntime-extensions builds for Java

#### Description:

This repository contains [Microsoft onnxruntime-extensions](https://github.com/microsoft/onnxruntime-extensions) builds for Java, enabling the use of custom operations and functionality not natively supported by ONNXRuntime. 

#### Features:

Extend [ONNXRuntime](https://github.com/microsoft/onnxruntime) with custom operations and functionality.
Easily integrate ONNX Runtime Extensions into your Java applications.
Compatible with a wide range of ONNX models.

#### Getting Started:

To use ONNX Runtime Extensions in your Java project, you can add it as a Maven dependency:

#### Usage:

##### install maven dependency locally 

````shell
cd onnxruntime-extensions-java
mvn clean install 
````
##### add the dependency to your pom.xml

````xml
<dependency>
    <groupId>com.hichemmaiza.onnx</groupId>
    <artifactId>onnxruntime-extensions-java</artifactId>
    <version>0.10.0-SNAPSHOT</version>
</dependency>
````

Here's a quick example of how to use ONNX Runtime Extensions in your Java code:

````java
public class DemoClass{

    private final OrtEnvironment ortEnvironment;
    private final OrtSession ortSession;
    public DemoClass(){
        ortEnvironment = OrtEnvironment.getEnvironment();
        sessionOptions = new OrtSession.SessionOptions();
        // here where you add the onnxruntime extensions
        sessionOptions.registerCustomOpLibrary(OrtxPackage.getLibraryPath());
    }
}
````

#### License:

This project is licensed under the MIT License - see the LICENSE file for details.