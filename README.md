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







