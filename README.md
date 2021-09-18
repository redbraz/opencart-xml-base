# 🇧🇷 opencart Base OCMOD/XML
 Arquivo base para criação de modificações em ocmod xml


### ATRIBUTOS

 - trim="(true|false)"						           -> Retira espaço no ínicio e final de uma string
 - regex="(true|false)"					           -> Retorna a expressão regular atual
 - index="(number)"						              -> indica a posição que deseja inserir caso tenha mais que 1
 - position="(replace|before|after)" 		-> indica como deseja inserir "subistituir, antes ou depois"
 - offset="(number)"						             -> indica quantas linhas deseja pular
 - limit="(number)"						              -> indica quantas vezes deseja executar (quando existir mais posições encontradas pela busca)
 - error="(log/skip/abort)"				        -> Envia uma mensagem de erro para as rotinas definidas para gerenciamento de erros ou termina o script

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
