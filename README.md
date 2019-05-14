# mitmproxy

## Setting up mitmproxy with Java 

1. Install mitmoproxy
   1. brew install mitmproxy
2. Download Portecle.
3. run mitmproxy once. [ Go to commandline type mitmproxy hit ENTER].
4. Your certificates will be generated in ~/.mitmproxy
5. Using portecle to  create a keystore with the mitmproxy-ca-cert.pem file.
6. Use the following commandline params to run your Java App

-Dhttp.nonProxyHosts=
-Dhttp.proxyHost=localhost
-Dhttp.proxyPort=8080
-Dhttps.proxyHost=localhost
-Dhttps.proxyPort=8080
-Dhttp.nonProxyHosts=
-Djavax.net.ssl.trustStore=/Users/<user>/trustcert
-Djavax.net.ssl.trustStorePassword=<YOUR_PASSWORD>

7. run mitmweb and you will see the requests from java .
