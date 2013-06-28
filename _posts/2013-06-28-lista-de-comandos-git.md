---
layout: post
title: Lista de comandos GIT
---

##Lista de comandos GIT

Configurações básicas e globais
* $ git config --global user.name "[seu nome]"
* $ git config --global user.email [seu e-mail]
* $ git config --global apply.whitespace nowarn
* $ git config --global core.whitespace nowarn
* $ git config --global color.branch auto
* $ git config --global color.diff auto
* $ git config --global color.status auto

#Alias
Com o alias, você pode criar apelidos aos comando fo GIT, para criar uma alias digite:

* $ git config --global alias.st status
* $ git config --global alias.co checkout

Para usar o comando, digite por exemplo:

* $ git st
* $ git co
#Criar repositório
* $ mkdir [pasta]
* $ cd pasta
* $ git init

#Criando e aplicando vários patch de um branch
* $ git checkout [branch]
* $ git format-patch --stdout master > patch
* $ git am --whitespace=nowarn patch
#Adicionar arquivo(s) ao próximo commit
* $ git add [arquivo1] [arquivo2] ...
ou para adicionar todos aquivos digite:

* $ git add .
# Fazer um commit com as mudanças
* $ git commit -m "[mensagem]"
# Criar um Branch
* $ git checkout -b [branch]
# Criar um branch baseado em outro branch específico
* $ git checkout -b [branch]
# Deletar um branch
* $ git branch -d [branch]
# Ver o branch atual
* $ git branch
# Trocar de Branch
* $ git checkout [branch]
# Clonar um repositório
* $ git clone [origin] [nova pasta]
# Atualizar repositório local
* $ git pull
# Enviar atualizações ao repositório remoto
* $ git push [origin] [branch]
# Visualizar arquivos alterados
* $ git status
# Verificar mudanças em arquivos adicionados (com git add)
* $ git diff
# Verifica mudanças entre commits
* $ git diff [ID1] [ID2]
# Histórico dos commits
* $ git log
# Verificar mudanças em um commit específico
* $ git show [ID]
# Verificar mudanças em um arquivo de um commit
* $ git show [ID] [arquivo]

# Voltando ao commit anterior descartando totalmente o commit atual
Cuidado com esse procedimento pois não há como recuperar!

* $ git reset --hard HEAD^
#Voltando ao commit anterior, mas criando um novo commit
* $ git revert HEAD

#Mesclar/Unir [branch1] ao [branch2]
* git checkout [branch2]
* git merge [branch1]
