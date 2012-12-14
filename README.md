<?php

  include("conexao.php");

	$nome = $_POST["nome"];
	$email = $_POST["email"];
	$telefone = $_POST["telefone"];

	if(empty($nome) or empty($email) or empty($telefone)){

	echo "Erro! Preencha todos os campos!";
	exit;

	}else{


	if(mysql_query("insert into tb_clientes (nome,email,telefone) VALUES('$nome','$email','$telefone')")){


	echo "Cadastrado com Sucesso!";

	exit;

	} else {

	echo mysql_error();
	exit;
	
	}
