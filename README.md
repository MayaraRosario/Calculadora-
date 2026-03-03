<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Calculadora Simples</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 50px;
    }
    input {
      width: 200px;
      padding: 10px;
      margin: 5px;
    }
    button {
      padding: 10px 15px;
      margin: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <h2>Calculadora Simples</h2>

  <input type="number" id="num1" placeholder="Primeiro número">
  <input type="number" id="num2" placeholder="Segundo número">
  <br>

  <button onclick="somar()">+</button>
  <button onclick="subtrair()">-</button>
  <button onclick="multiplicar()">*</button>
  <button onclick="dividir()">/</button>

  <h3>Resultado: <span id="resultado"></span></h3>

  <script>
    function somar() {
      let n1 = Number(document.getElementById("num1").value);
      let n2 = Number(document.getElementById("num2").value);
      document.getElementById("resultado").innerText = n1 + n2;
    }

    function subtrair() {
      let n1 = Number(document.getElementById("num1").value);
      let n2 = Number(document.getElementById("num2").value);
      document.getElementById("resultado").innerText = n1 - n2;
    }

    function multiplicar() {
      let n1 = Number(document.getElementById("num1").value);
      let n2 = Number(document.getElementById("num2").value);
      document.getElementById("resultado").innerText = n1 * n2;
    }

    function dividir() {
      let n1 = Number(document.getElementById("num1").value);
      let n2 = Number(document.getElementById("num2").value);
      
      if (n2 === 0) {
        document.getElementById("resultado").innerText = "Não é possível dividir por zero";
      } else {
        document.getElementById("resultado").innerText = n1 / n2;
      }
    }
  </script>

</body>
</html>
