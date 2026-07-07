# toolnest
free online tools website
<!DOCTYPE html>
<html>
<head>
<title>Age Calculator</title>
<style>
body{
font-family:Arial;
text-align:center;
padding:30px;
}
input,button{
padding:10px;
margin:10px;
font-size:18px;
}
</style>
</head>
<body>

<h1>Age Calculator</h1>

<input type="date" id="dob">
<br>
<button onclick="age()">Calculate Age</button>

<h2 id="result"></h2>

<script>
function age(){
let dob=new Date(document.getElementById("dob").value);
let today=new Date();

let years=today.getFullYear()-dob.getFullYear();

if(
today.getMonth()<dob.getMonth() ||
(today.getMonth()==dob.getMonth() && today.getDate()<dob.getDate())
){
years--;
}

document.getElementById("result").innerHTML="Your Age is "+years+" years";
}
</script>

</body>
</html>
