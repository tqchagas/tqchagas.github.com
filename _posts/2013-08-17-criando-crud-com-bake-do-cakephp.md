---
layout: post
title: Criando CRUD com Bake do CakePHP
author: Thiago Chagas
categories: [cakephp, bake, crud]
description: "Guia de como criar um CRUD usando o Bake do CakePHP"
---
### Introdução

Baixe a última versão estável do [CakePHP[](http://cakephp.org/) - Atualmente 2.3.9

Neste tutorial iremos usar o SGBD Mysql, certifique de ter ele instalado.


Em /seu_projeto/app/app/Config/ crie um arquivo chamado database.php, com o seguinte conteudo (adaptando o mesmo a sua realidade):

<pre><code>class DATABASE_CONFIG {

	public $default = array(
		'datasource' => 'Database/Mysql',
		'persistent' => false,
		'host' => 'localhost',
		'login' => 'root',
		'password' => '',
		'database' => 'cake',
		'encoding' => 'utf8',
	);
}</code></pre>

No Mysql, crie um DB e utilize o seguinte código para criar a tabela:
<pre><code>CREATE TABLE posts (
    id INT UNSIGNED AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(50),
    body TEXT,
    created DATETIME DEFAULT NULL,
    modified DATETIME DEFAULT NULL
);</code></pre>

Agora no terminal, digite o seguinte código:
php /nome_projeto/app/Console/cake.php bake

Você vai se deparar com o seguinte conteúdo:
<img src="http://thiagochagas.com/assets/imagens/bake.png" alt="Bake">

### Criando o Model
Iremos começar configurando o Model, para isso pressione M e dê enter. A primeira pergunta é sobre qual Model iremos criar, digite 1. A próxima é sobre validações dos campos, pressione y e faça a configuração a seu gosto, caso não queira configurar, pressione n. A próxima pergunta é se o CRUD terá relações hasMany, hasOne, ou belongsTo, responda não. Na próxima pergunta confirme a criação e quando perguntado sobre PHPUnit, responda negativamente.

### Criando o Controller
Digite C e então será levado para a area de criação dos Controllers.
Primeira pergunta é questionando qual Controller iremos criar, digite 1. Responda não na pergunta sobre Controller interativamente. A próxima pergunta é se desejamos criar os métodos para criar, listar, editar e deletar, responda sim. Responda não na pergunta seguinte. Confirme a criação do Controller, e responda não na pergunta sobre PHPUnit.

### Criando as Views
Pressione V para poder criar as Views.
Primeira pergunta é sobre qual tabela iremos criar as views, informe 1. Responda que sim, deseja criar as views interativamente. Responda que sim, deseja criar as views do CRUD. Responda que não e pronto, já tem um CRUD funcionando.

Ao acessar http://127.0.0.1/nome_projeto/posts você será capaz de visualizar o CRUD.

<h5>{{ page.date | date: "%d/%m/%Y" }} by {{ page.author }}</h5>
