# Welcome to my Node.js notes!

Hi! My name is Himal  Rawal . Here I will be taking notes about the **errors and issues**  that I have  faced during learning node js wih their solutuions.


## My First Issue: CORS

I got Following error while connecting node js api  in  React front end.

    Access to XMLHttpRequest at 'http://localhost:3000/auth/login' from origin 'http://localhost:3001' has been blocked by CORS policy: Response to preflight request doesn't pass access control check: The value of the 'Access-Control-Allow-Credentials' header in the response is '' which must be 'true' when the request's credentials mode is 'include'. The credentials mode of requests initiated by the XMLHttpRequest is controlled by the withCredentials attribute.

**Solution:**

 

 - Install  cors package using 

> npm i cors

 - And use below code in app.js
```
    //import cors
    var  cors = require('cors')
    
    var  corsOptions = {
    origin:  'http://localhost:3001',
    optionsSuccessStatus:  200,
    credentials:  true,
    }
    app.use(cors(corsOptions))

```
To Know root cause of error read:
[read this](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS),
[And this stackoverflow question](https://stackoverflow.com/questions/18642828/origin-origin-is-not-allowed-by-access-control-allow-origin)
