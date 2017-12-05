# ESPAsyncHttpClient
A very basic asynchronous HTTP client for the ESP8266 that uses ESPAsyncTCP. it was written for a very specific need, so it is not a truly general class.

This code is provided as-is. I am more than happy for anyone to take it and use it, or turn it into an actual general library.

## Example
```c++
  AsyncHTTPClient httpClient;
  
  void readSucceeded() {
	  String body = httpClient.getBody();
    ...
  }
  
  void readFailed(String msg) {
	  DEBUG(msg);
  }

  void loop() {
    ...
    httpClient.initialize("http://www.google.com/");
    ...
    httpClient.makeRequest(readSucceeded, readFailed);
  }
```
