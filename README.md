# electron_js_desktop
Build a desktop app using Electron, which lets you create applications with web technologies like HTML, CSS, and JavaScript. Just set up your project, write a main file to create a window, and design your app's interface using HTML

Follow above step's:-
1.Create the folder .i.e. electron and open in vscode

2.In VS code open terminal and enter the npm init -y

this command download the package.json file

3.Again in terminal type npm install electron

4.Create the main.js file and hello.html file 

5. main.js :-


           
const {app,BrowserWindow}=require('electron');
app.whenReady().then(() =>{
    const mainWindow=new BrowserWindow({
        width:800,
        height:800
    });
    mainWindow.loadFile('hello.html');
});

6. hello.html:-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration form</title>
</head>
<body>
   
    <form id="reg" action="" >
        <center>
            <h1>Registration Form</h1>
            <input type="text" id="name" value="" placeholder="Enter the name" required><br></br>
            <input type="text" id="roll" value="" placeholder="Enter the rollno" required><br></br>
            <input type="text" id="city" value="" placeholder="Enter the city" required><br></br>
            <input type="tel" id="num" value="" maxlength="10" placeholder="Enter the number" required><br></br>
            <input type="text" id="pass" value="" placeholder="Enter the password" required><br></br>
            <input type="reset" value="reset"><br></br>
            <input type="submit" value="submit">
        </center>
    </form>
   
</body>
</html>

7.make change in package.json file 
i.e.
"main": "main.js",
  "scripts": {
    "start": "electron main.js"
  },

8.package.js-
{
  "name": "ele",
  "version": "1.0.0",
  "description": "",
  "main": "main.js",
  "scripts": {
    "start": "electron main.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "electron": "^25.2.0"
  }
}
9. last enter the command in terminal 
npm start


it open the registration in electron format
