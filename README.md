# OAuth-Authorization-Server-demo

A very simple web application to upload files into google drive using PHP, JS and Google Drive API version 2.

Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

Prerequisites
This project is web-based. Therefore you need to set up a web server on your local machine.

Installation
Create a new project in your web root. Copy all files & directories inside this repository into your project folder.
1. css
    - submit.css
2. js
    - core.js
    - submit.js
3. modules
    - submit.html
4. index.html
Create a web project OAuth Client ID in Google Developers Console and get your client id and client secret.
For authorized JavaScript origins, just provide localhost for the first field and the second field is important it needs to be the same for your project you can have different redirect URL. It is basically the URL to which Google redirects you whenever the user grants access to your application. Select it cautiously it needs to be the same for your project.

Make sure that you have enabled API services (Guide).

After that, edit the file core.js which will hold the logic for index.html. In this file, we will redirect the user to the permissions page where users can grant access to your application.
     // client id of the project

     var clientId = "";

     // redirect_uri of the project

     var redirect_uri = "";

     // scope of the project

     var scope = "https://www.googleapis.com/auth/drive";

     // the URL to which the user is redirected to

     var url = "";
Edit submit.js
 const urlParams = new URLSearchParams(window.location.search);
    const code = urlParams.get('code');
    const redirect_uri = "" // replace with your redirect_uri;
    const client_secret = ""; // replace with your client secret
    const scope = "https://www.googleapis.com/auth/drive";
    var access_token= "";
    var client_id = ""// replace it with your client id;
