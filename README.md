<html>
<head>
<title>Javascript Login Form Validation</title>
<!-- Include CSS File Here -->
<style>@import url(http://fonts.googleapis.com/css?family=Raleway);
h2{
background-color: #FEFFED;
padding: 30px 35px;
margin: -10px -50px;
text-align:center;
border-radius: 10px 10px 0 0;
}
hr{
margin: 10px -50px;
border: 0;
border-top: 1px solid #ccc;
margin-bottom: 40px;
}
div.container{
width: 900px;
height: 610px;
margin:35px auto;
font-family: 'Raleway', sans-serif;
}
div.main{
width: 300px;
padding: 10px 50px 25px;
border: 2px solid gray;
border-radius: 10px;
font-family: raleway;
float:left;
margin-top:50px;
}
input[type=text],input[type=password]{
width: 100%;
height: 40px;
padding: 5px;
margin-bottom: 25px;
margin-top: 5px;
border: 2px solid #ccc;
color: #4f4f4f;
font-size: 16px;
border-radius: 5px;
}
label{
color: #464646;
text-shadow: 0 1px 0 #fff;
font-size: 14px;
font-weight: bold;
}
center{
font-size:32px;
}
.note{
color:red;
}
.valid{
color:green;
}
.back{
text-decoration: none;
border: 1px solid rgb(0, 143, 255);
background-color: rgb(0, 214, 255);
padding: 3px 20px;
border-radius: 2px;
color: black;
}
input[type=button]{
font-size: 16px;
background: linear-gradient(#ffbc00 5%, #ffdd7f 100%);
border: 1px solid #e5a900;
color: #4E4D4B;
font-weight: bold;
cursor: pointer;
width: 100%;
border-radius: 5px;
padding: 10px 0;
outline:none;
}
input[type=button]:hover{
background: linear-gradient(#ffdd7f 5%, #ffbc00 100%);
}
.downloads{visibility: hidden;}
</style>
<!-- Include JS File Here -->
<script>
    var attempt = 3; // Variable to count number of attempts.
// Below function Executes on click of login button.
function validate(){
var username = document.getElementById("username").value;
var password = document.getElementById("password").value;
if ( username == "1" && password == "1"){
showdownloads()
hidelogin()
return false;
}
else{
attempt --;// Decrementing by one.
alert("You have left "+attempt+" attempt;");
// Disabling fields after 3 attempts.
if( attempt == 0){
document.getElementById("username").disabled = true;
document.getElementById("password").disabled = true;
document.getElementById("submit").disabled = true;
return false;
}
}
}
    function showdownloads() {
    var hid = document.getElementsByClassName("downloads");
    if(hid[0].offsetWidth > 0 && hid[0].offsetHeight > 0) {
        hid[0].style.visibility = "visible";
    }
}

    function hidelogin() {
    var hid = document.getElementsByClassName("login");
    if(hid[0].offsetWidth > 0 && hid[0].offsetHeight > 0) {
        hid[0].style.visibility = "hidden";
    }
}
</script>
</head>
<div class="downloads">
    <h1>Downloads:</h1>
    <p>Powershell BAT file:</p>
    <a href="https://drive.google.com/file/d/1lJ8XcJJkn0NkY4is-d8esWgd8-PiFcMY/view?usp=drive_link">.bat file</a>
    </div>
<div class="login">
<body>
<div class="container">
<div class="main">
<h2>Login to see files</h2>
<form id="form_id" method="post" name="myform">
<label>User Name :</label>
<input type="text" name="username" id="username"/>
<label>Password :</label>
<input type="password" name="password" id="password"/>
<input type="button" value="Login" id="submit" onclick="validate()"/>
</form>
</div>
</div>
</div>
</body>


</html>
