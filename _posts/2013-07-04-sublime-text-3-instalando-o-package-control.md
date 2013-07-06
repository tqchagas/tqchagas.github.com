---
layout: post
title: Sublime Text 3 - Como instalar o Package Control e Plugins
author: Thiago Chagas
categories: [sublime text 3, control package]
description: "Guia de como instalar o Control Package e outros plugins no Sublime Text 3."
---

Atualmente, o Sublime Text 3 está em fase Beta, [visite a página do sublime](http://www.sublimetext.com/3), faça o download e a instalação.

Caso não tenha o Git instalado, faça o [download](http://git-scm.com/downloads). No momento da instalação, marque: "Windows Exlporer Integration > Simple Context Menu" e "Run Git from the Windows Command Prompt".

Após a instalação do sublime, abra o editor, vá em Preferences > Browse Packages, dê um clique com o botão direito e selecione "Git Bash Here". Agora no Git, execute o código abaixo:
<pre><code>git clone https://github.com/wbond/sublime_package_control.git "Package Control"
cd "Package Control"
git checkout python3</code></pre>
<!-- break -->

Pronto, nesse momento você já tem o Control Package instalado.

Agora basta reiniciar o ST3, CTRL+SHIFT+P > Install e instalar os seus Plugins preferidos.

Infelizmente, nem todos os plugins estão rodando, como é o caso do SublimeCodeIntel, AutoFileName e outros. Consulte [aqui](https://github.com/wbond/sublime_package_control/wiki/Sublime-Text-3-Compatible-Packages) as compatibilidades de pacotes do ST3.

###Alguns plugins que recomendo

####Emmet
Instalação: CTRL + SHIFT + P > Install > Emmet

Confira todos os atalhos disponiveis: http://docs.emmet.io/cheat-sheet/

####File History
Instalação: CTRL + SHIFT + P > Install > File History

Mais sobre a utilização: https://github.com/FichteFoll/sublimetext-filehistory


<h5>{{ page.date | date: "%d/%m/%Y" }} by {{ page.author }}</h5>