# **외부 API를 호출하는 함수를 pseudocode로 작성 및 설명**

### 예제 pseudocode



```javascript
function callAPI(url, method, data) {
  // 1. HTTP 요청 객체 생성합니다.
  let request = new XMLHttpRequest();
  request.open(method, url);

  // 2. 요청 헤더 설정합니다.
  request.setRequestHeader("Content-Type", "application/json");

  // 3. 요청 데이터 설정합니다.
  if (data) {
    request.setRequestHeader("Content-Length", Buffer.byteLength(data));
    request.send(data);
  } else {
    request.send();
  }

  // 4. 요청을 받습니다.
  request.onload = () => {
    if (request.status === 200) {
      // 5. 응답 데이터를 반환합니다.
      return JSON.parse(request.responseText);
    } else {
      // 6. 에러를 반환합니다.
      return new Error(request.statusText);
    }
  };
}

```
