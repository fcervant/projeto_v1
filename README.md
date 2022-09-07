# projeto_v1
Projeto do curso TEX-JavaScript DevOps - GitHUB

# Primeiro passo - clonando o repositorio

fernandorc@fernandorc-VirtualBox:~/Documentos$ git clone https://github.com/fcervant/projeto_v1.git
Cloning into 'projeto_v1'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 634 bytes | 158.00 KiB/s, done.

# Abrir o folder do projeto no VSCode

# Os comandos executados foram incluidos no arquivo README.md
# Agora é criar um novo branch para executar as alterações

fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git checkout -b frc_projeto_v1
Switched to a new branch 'frc_projeto_v1'

# checando os branches - o comando acima já deixa posicionado no branch criado

fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git branch
* frc_projeto_v1
  main
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ 

# no git remoto esta branch não existe, somente no local - executar então o comando abaixo para criar no remoto tb. Utilizar os ajustes neste arquivo para o commit

fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git add -A
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git status
No ramo frc_projeto_v1
Mudanças a serem submetidas:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md

fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git commit -m "criação branch frc_projeto_v1"
[frc_projeto_v1 14c15c1] criação branch frc_projeto_01
 1 file changed, 30 insertions(+)
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ 

fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git push origin frc_projeto_v1
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 844 bytes | 844.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'frc_projeto_v1' on GitHub by visiting:
remote:      https://github.com/fcervant/projeto_v1/pull/new/frc_projeto_v1
remote: 
To https://github.com/fcervant/projeto_v1.git
 * [new branch]      frc_projeto_v1 -> frc_projeto_v1
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ 

# o branch agora também está no git remoto


# renomeando o branch caso necessário

fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git branch
* frc_projeto_v1
  main
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git branch -m frc_projeto_v2
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git branch
* frc_projeto_v2
  main
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ 

# em caso de alteração no nome da branch, a mesma precisa ser atualizada no git remoto, repetir o processo anterior (add, commit). Porém antes do push do branch renomeado é necessário remover o branch anterior.

fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git branch
* frc_projeto_v1
  main
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git branch -m frc_projeto_v2
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git branch
* frc_projeto_v2
  main
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git push origin --delete frc_projeto_v1
To https://github.com/fcervant/projeto_v1.git
 - [deleted]         frc_projeto_v1

fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git push origin frc_projeto_v2
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 2 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 1.49 KiB | 1.49 MiB/s, done.
Total 6 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'frc_projeto_v2' on GitHub by visiting:
remote:      https://github.com/fcervant/projeto_v1/pull/new/frc_projeto_v2
remote: 
To https://github.com/fcervant/projeto_v1.git
 * [new branch]      frc_projeto_v2 -> frc_projeto_v2
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ 

# agora é possível continuar trabalhando na versão do branch atual - frc_projeto_v2, sempre que ocorrer uma alteração executar o mesmo processo - status, add, commit, push com a opção HEAD>branch

fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git status
No ramo frc_projeto_v2
Changes not staged for commit:
  (utilize "git add <arquivo>..." para atualizar o que será submetido)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Arquivos não monitorados:
  (utilize "git add <arquivo>..." para incluir o que será submetido)
        info.txt

nenhuma modificação adicionada à submissão (utilize "git add" e/ou "git commit -a")
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git add -A
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git commit -m "Atualizando novo arquivo info.txt"
[frc_projeto_v2 ef59b1b] Atualizando novo arquivo info.txt
 2 files changed, 32 insertions(+), 1 deletion(-)
 create mode 100644 info.txt
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ 

fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git push origin HEAD:frc_projeto_v2
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 817 bytes | 272.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/fcervant/projeto_v1.git
   ef59b1b..b50f4d8  HEAD -> frc_projeto_v2
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ 


# checando os branches no git remoto
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git branch -r
  origin/HEAD -> origin/main
  origin/frc_projeto_v2
  origin/main
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ 

# fazendo checkout direto no branch remoto

fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git checkout origin/frc_projeto_v2
M       README.md
Note: switching to 'origin/frc_projeto_v2'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at b50f4d8 Atualizando ajustes arquivo README.md
fernandorc@fernandorc-VirtualBox:~/Documentos/projeto_v1$ git checkout origin/frc_projeto_v2




