# 🇧🇷 opencart Base OCMOD/XML
 Arquivo base para criação de modificações em ocmod xml


### ATRIBUTOS

 - trim="(true|false)" - *Retira espaço no ínicio e final de uma string.*
   - true -- retiras os espaços
   - false -- mantem espaços 
 - regex="(true|false)" - *Retorna a expressão regular atual.*
   -  true -- verdadeiro
   -  false -- falso
 - index="(number)" - *indica a posição que deseja inserir caso tenha mais que 1 correspondência do elemento buscado.*
   - Ex: se estiver buscado por "form" e tiver 3 forms no mesmo arquivo indique qual deles deseja pegar. 
 - position="(replace|before|after)" - *indica como deseja inserir (subistituir, antes ou depois).*
   - replace -- substitui o elemento buscado pelo novo elemento
   - before -- adiciona antes do elemento buscado
   - after -- adicona apos o elemento buscado 
 - offset="(number)" - *indica quantas linhas deseja pular apartir da insersão.*
   - Ex: se estou buscando um elemento especifico e preciso pular x linhas após ele, logo eu indico isso com o parametro offset. 
 - limit="(number)" - *indica quantas vezes deseja executar (quando existir mais posições encontradas pela busca)*
   - Indica o limite de modificações caso exista muitos outros elementos iguais a busca.
 - error="(log/skip/abort)" - *Envia uma mensagem de erro para as rotinas definidas para gerenciamento de erros ou termina o script.*
   - log -- gera o relatório no console de saida caso tenha erros
   - skip -- não gera nenhum relatório no console de erros
   - abort -- para de executar o script caso encontre um erro.

###  Base XML

```
<?xml version="1.0" encoding="utf-8"?>
<modification>
  <name>NAME MODIFICATION</name>
  <code>CODIGO MODIFICATION</code>
 	<version>1.0</version>
	<author>Author</author>
	<link>https://www.link.com/</link>
	
	<file path="">
		<operation error="log">
			<ignoreif regex="true"><![CDATA[ ]]></ignoreif>
			<search><![CDATA[ ]]></search>
			<add position="before"><![CDATA[ ]]></add>
		</operation>
	</file>
</modification>
```
