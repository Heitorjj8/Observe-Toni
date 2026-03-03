# Observe-Toni
<form action="processa.php" method="POST">
    Nome: <input type="text" name="nome" required><br><br>
    Endereço: <input type="text" name="endereco" required><br><br>
    Idade: <input type="number" name="idade" required><br><br>
    Sexo: 
    <input type="radio" name="sexo" value="Masculino" checked> Masculino
    <input type="radio" name="sexo" value="Feminino"> Feminino<br><br>
    <input type="submit" value="Enviar">
</form>

<?php
$usuario = $_POST['usuario'];
$senha = $_POST['senha'];

if ($usuario == "aluno" && $senha == "123") {
    echo "Bem-vindo, " . $usuario . "! Seu cargo é: Estudante de Informática.";
} else {
    echo "Erro: Nome de usuário ou senha incorretos!";
}
?>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>sla</title>
</head>
<body>
    <form action="pagina_protegida.php" method="POST">
        Usuário: <input type="text" name="usuario" required><br><br>
     Senha: <input type="password" name="senha" required><br><br>
    <button type="submit">Entrar</button>
</form>
</body>
</html>
<?php
$Noome = $_POST['nome'];
$endereco = $_POST['endereco'];
$idade = $_POST['idade'];
$sexo = $_POST['sexo'];

echo "Nome: $Noome ";

if ($idade >= 18) {
    echo "Minha idade é:  $idade ";
    echo "Sexo:  $sexo ";
    echo "Endereço:  $endereco";
} else {
    echo "Menor de idade";
}
?>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ex3</title>
</head>
<body>
    <form action="calcula_nota.php" method="POST">
    Média Final: <input type="number" step="0.1" name="mf" required><br><br>
    <button type="submit">Calcular</button>
</form>
</body>
</html>
<?php
$mf = $_POST['mf'];

if ($mf <= 1.7) {
    echo "Sua média é " . $mf . ". Você não poderá realizar o exame.";
} 
elseif ($mf >= 7.0) {
    echo "Sua média é " . $mf . ". Você está APROVADO!";
} 
else {
    $ne = (50 - ($mf * 6)) / 4;
    echo "Sua média é " . $mf . ". Você está em exame.<br>";
    echo "Nota necessária no exame: " . $ne;
}
?>
