# CS305-Software-Security

<b> Who was the client and what issue did they want to address? </b>

Artemis Financial is a fictional consulting company that creates financial plans for their clients. They wanted to include a file verification step to their application in the form of a checksum verification and to have secure communications between the client and the server. Their requirements for this were to implement an algorithm cipher into the code by writing a @RequestMapping method, confirm functionality by performing a checksum verification, generate a self-signed certificate using the command prompt, refactor the code base to convert from HTTP tto HTTPS protocol, perform secondary testing with dependency cheks, and perform functional testing by manually reviewing the code.

<b> How did you increase layers of security? </b>

To add layers of security, the code was refactored by using the MessageDigest library and a bytes to hex function to implement the SHA-256 cryptographic hash algorithm. The @RequestMapping method was used to create a RESTful route to the web browser. In order to convert from an HTTP to an HTTPS protocol, I generated a self-signed certificate and installed it to my machine as a trusted root certificate authority. Then I added keystore.jks to the project and refactored the code in the application.properties file with the correct entries to enable HTTPS with the SSL keystore.

<b> How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities? </b>

To make sure that the code was functional and secure, the code was compiled and checked for successful execution. Upon visiting the localhost site, correct implementation of SHA-256 and the HTTPS protocol was verified. To check for new vulnerabilities, a dependency check was run before and after refactoring the code to ensure that no new vulnerabilities were introduced and functional testing through a manual code review was conducted to identify any additional vulnerabilities.

<br>

<b> Tools Used </b>

&emsp;• Spring Framework
<br>
&emsp;• Maven plugin
<br>
&emsp;• OWASP Dependency Check
