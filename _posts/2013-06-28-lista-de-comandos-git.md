---
layout: post
title: Lista de comandos GIT
author: Thiago Chagas
---

####Configurações básicas e globais
<h5>{{ post.date | date: "%d/%m/%Y" }} by {{ page.author }}</h5>
<pre><code>$ git config --global user.name "[seu nome]"
$ git config --global user.email [seu e-mail]
$ git config --global apply.whitespace nowarn
$ git config --global core.whitespace nowarn
$ git config --global color.branch auto
$ git config --global color.diff auto
$ git config --global color.status auto</code></pre>

<!-- break -->
####Alias
Com o alias, você pode criar apelidos aos comando fo GIT, para criar uma alias digite:

<pre><code>$ git config --global alias.st status
$ git config --global alias.co checkout</code></pre>

####Para usar o comando, digite por exemplo:

<pre><code>$ git st
$ git co</code></pre>


####Criar repositório

<pre><code>$ mkdir [pasta]
$ cd pasta
$ git init</code></pre>


####Criando e aplicando vários patch de um branch

<pre><code>$ git checkout [branch]
$ git format-patch --stdout master > patch
$ git am --whitespace=nowarn patch</code></pre>
####Adicionar arquivo(s) ao próximo commit

<pre><code>$ git add [arquivo1] [arquivo2] ...</code></pre>
ou para adicionar todos aquivos digite:

<pre><code>$ git add .</code></pre>
#### Fazer um commit com as mudanças
<pre><code>$ git commit -m "[mensagem]"</code></pre>
#### Criar um Branch
<pre><code>$ git checkout -b [branch]</code></pre>
#### Criar um branch baseado em outro branch específico
<pre><code>$ git checkout -b [branch]</code></pre>
#### Deletar um branch
<pre><code>$ git branch -d [branch]</code></pre>
#### Ver o branch atual
<pre><code>$ git branch</code></pre>
#### Trocar de Branch
<pre><code>$ git checkout [branch]</code></pre>
#### Clonar um repositório
<pre><code>$ git clone [origin] [nova pasta]</code></pre>
#### Atualizar repositório local
<pre><code>$ git pull</code></pre>
#### Enviar atualizações ao repositório remoto
<code>$ git push [origin] [branch]</code>
#### Visualizar arquivos alterados
<pre><code>$ git status</code></pre>
#### Verificar mudanças em arquivos adicionados (com git add)
<pre><code>$ git diff</code></pre>
#### Verifica mudanças entre commits
<pre><code>$ git diff [ID1] [ID2]</code></pre>
#### Histórico dos commits
<pre><code>$ git log</code></pre>
#### Verificar mudanças em um commit específico
<pre><code>$ git show [ID]</code></pre>
#### Verificar mudanças em um arquivo de um commit
<pre><code>$ git show [ID] [arquivo]</code></pre>

#### Voltando ao commit anterior descartando totalmente o commit atual
Cuidado com esse procedimento pois não há como recuperar!

<pre><code>$ git reset --hard HEAD^</code></pre>
####Voltando ao commit anterior, mas criando um novo commit
<pre><code>$ git revert HEAD</code></pre>

####Mesclar/Unir [branch1] ao [branch2]
<pre><code>$ git checkout [branch2]
$ git merge [branch1]</code></pre>