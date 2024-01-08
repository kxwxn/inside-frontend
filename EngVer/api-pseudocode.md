# **Write a pseudocode for a function that calls an external API.**

### example code



```javascript
function callAPI(url, method, data) {
  // 1. Create an HTTP request object.
  let request = new XMLHttpRequest();
  request.open(method, url);

  // 2. Set the request headers.
  request.setRequestHeader("Content-Type", "application/json");

  // 3. Set the request data.
  if (data) {
    request.setRequestHeader("Content-Length", Buffer.byteLength(data));
    request.send(data);
  } else {
    request.send();
  }

  // 4. Receive the response.
  request.onload = () => {
    if (request.status === 200) {
      // 5. Return the response data.
      return JSON.parse(request.responseText);
    } else {
      // 6. Return an error.
      return new Error(request.statusText);
    }
  };
}

```
