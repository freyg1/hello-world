# hello-world
KETE - Projekt
<!DOCTYPE html>
<html>
<!--   Example GetIPAddress.html by JSON object -->
<!--   KETE LB6a - Web Services            -->
<!--   V1 / 24.09.2020 / dbe   initial     -->

<head>
  <title>Display IP Address</title>
  <style>
    body {
      background-color: #FFCC00;
    }

    h1 {
      font-family: sans-serif;
      text-align: center;
      padding-top: 140px;
      font-size: 60px;
      margin: -15px;
    }

    p {
      font-family: sans-serif;
      color: #907400;
      text-align: center;
    }
  </style>
</head>

<body>
  <h1 id=ipText></h1>
  <p>( This is your IP address...probably :-) )</p>
  <script>
    fetch("https://ipinfo.io/json")
      .then(function (response) {
        return response.json();
      })
      .then(function (myJson) {
        document.querySelector("#ipText").innerHTML = myJson.ip;
      })
      .catch(function (error) {
        console.log("Error: " + error);
      });
  </script>
</body>

</html>  
