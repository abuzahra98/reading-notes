# WRRC and Java

## HTTP Request Lifecycle

Java Class for HTTP requests is `HttpUrlConnection` and allows for basic HTTP requests.

Method for creating an *instance* of `HttpUrlConnection` is `openConnection()`. Creates a connection object but does not actually establish it.

`requestMethod` attribute allows for requests with the addition of values `GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.`

```JAVA
URL url = new URL("http://example.com");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");
```

Parameters can be added to a request by setting the `doOutput` property to true and write a string to the OutputStream `HttpUrlConnection` instance.

```JAVA
Map<String, String> parameters = new HashMap<>();
parameters.put("param1", "val");

con.setDoOutput(true);
DataOutputStream out = new DataOutputStream(con.getOutputStream());
out.writeBytes(ParameterStringBuilder.getParamsString(parameters));
out.flush();
out.close();

public class ParameterStringBuilder { // Transforms a MAP into a formatted STRING
    public static String getParamsString(Map<String, String> params) 
      throws UnsupportedEncodingException{
        StringBuilder result = new StringBuilder();

        for (Map.Entry<String, String> entry : params.entrySet()) {
          result.append(URLEncoder.encode(entry.getKey(), "UTF-8"));
          result.append("=");
          result.append(URLEncoder.encode(entry.getValue(), "UTF-8"));
          result.append("&");
        }

        String resultString = result.toString();
        return resultString.length() > 0
          ? resultString.substring(0, resultString.length() - 1)
          : resultString;
    }
}
```

## High-level HTTP:
The HTTP Request Lifecycle:(1)

* Local Processing
* Resolve an IP
* Establish a TCP Connection
* Send an HTTP Request
* Tearing Down and Cleaning Up


Local Processing

Browser will then go through its own cache of recently accessed URLs, the operating system’s cache of recent queries, router’s cache, and DNS cache to extract the “scheme”/protocol, host, optional port number, resource path, and query strings that are given in the form.

Resolve an IP

If the cache lookup fails, the browser sends a UDP3 DNS request to its target DNS server. If a response isn’t received, the request will be forwarded to another server. This is because the server looks for the address associated with the requested hostname and sends a response. If it doesn’t arrive, the client has no idea how long it will take.



Establish a TCP Connection


Before the server can accept a three-way handshake, the client must first create a TCP connection. The server must be listening on a port and executing a passive open, after which the client can conduct an active open and the client-server connection will be recognized. This allows the receiver to restore the original order of received packets and the sender to restore the original order of sent packets.



[<== Back to Readme](README.md)