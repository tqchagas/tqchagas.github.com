---
layout: post
title: Sublime Text 3 - Como instalar o Package Control e Plugins
author: Thiago Chagas
categories: [sublime text 3, control package]
description: "Guia de como instalar o Control Package e outros plugins no Sublime Text 3."
---

Atualmente, o Sublime Text 3 está em fase Beta, [visite a página do sublime](http://www.sublimetext.com/3) e faça o download e instale.

Após a instalação, abra o editor, vá em Preferences > Browse Packages, no diretorio que abrir, dê um Git Bash Here, agora no Git Bash, execute o código abaixo:
<pre><code>git clone https://github.com/wbond/sublime_package_control.git "Package Control"
cd "Package Control"
git checkout python3</code></pre>
<!-- break -->

Pronto, agora basta abrir o ST3, CTRL+SHIFT+P, Install Package e instalar os seus Packages preferidos. Consulte [aqui](https://github.com/wbond/sublime_package_control/wiki/Sublime-Text-3-Compatible-Packages) as compatibilidades de pacotes do ST3.

Infelizmente, nem todos os plugins estão rodando, como o SublimeCodeIntel.

###Alguns plugins que recomendo

####Emmet
Instalação: CTRL + SHIFT + P > Install > Emmet
Confira todos os atalhos disponiveis: http://docs.emmet.io/cheat-sheet/

<h5>{{ page.date | date: "%d/%m/%Y" }} by {{ page.author }}</h5>
