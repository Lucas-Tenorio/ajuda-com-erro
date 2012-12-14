<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Lista de Clientes</title>
</head>

<body>
<?php

  include("conexao.php");

	$sql = mysql_query("select * from tb_clientes order by nome asc ");

	while($exibe = mysql_fetch_assoc($sql));

	echo "<a href'#'>Editar</a>";
	echo $exibe ["id"]." | ";
	echo utf8_encode($exibe ["nome"])." | ";
	echo utf8_encode($exibe ["email"])." | ";
	echo $exibe ["telefone"]." | ";
	echo "<a href'#'>Remover</a> <br>";



	endwhile;


?>




</body>
</html>
