<! DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Formulário de E-mail</title>
<style>
body {
background-color: pale;
color: black;
font-family: Arial, sans-serif;
}

h1 {
text-align: center;
color: red;
}

form {
margin: auto;
width: 40%;
padding: 50px;
background-color: #ffffff;
border-radius: 10px;
box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.2);
}

label {
display: block;
margin-bottom: 10px; 
}
input[type="email"] {
width: 90%;
padding: 10px;
margin-bottom: 20px;
border-radius: 5px;

}
input[type="submit"] {
background-color: #800;
color: #fff;
border: none;
padding: 10px 20px;
border-radius: 5px;
cursor: pointer;
}
input[type="submit"]:hover {
background-color: #330055;
}
</style>
</head>

<body>

<h1>Formulário de E-mail</h1>

<form onsubmit="return validarEmail()">
<label for="email">Insira seu E-mail:</label>
<input type="email" id="email" name="email" placeholder="seuemail@dominio.com">
<input type="submit" value="Enviar">
</form>

<script>
function validarEmail() {
var email = document.getElementById("email").value;
var regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
if (!regex.test(email)) {
alert("Por favor, insira um endereço de e-mail válido.");
return false;
}
alert("E-mail adicionado com sucesso : " + email);
return true;
}
</script>
</body>
</html>
