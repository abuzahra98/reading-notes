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

[<== Back to Readme](README.md)