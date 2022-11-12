https://aws.amazon.com/getting-started/hands-on/create-continuous-delivery-pipeline/module-one/

In this module you will set up a repository for your code so it can be easily accessed over the Internet. 
In this example we will be using GitHub, but there are other Git-compatible options you can use including AWS CodeCommit. 
In one of the following modules you will connect this hosted repo to our pipeline, 
so every time you push a new commit to it your build process is started.


Forked : https://github.com/aws-samples/aws-elastic-beanstalk-express-js-sample
Clone it and push with some changes inside the `app.js` 

checked the app.js file which basically `GET(HTTPS)` all the files 

const express = require('express');
const app = express();
const port = 8080;

app.get('/', (req, res) => res.send('Checking this feature - Balaji '));

app.listen(port);
console.log(`App running on http://localhost:${port}`);


pushed the code
can see the changes in the git forked repo 

--- module 1 completed --- 

