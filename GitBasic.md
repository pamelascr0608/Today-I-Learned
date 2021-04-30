# 💻 Comandos básicos para GIT

##### Referências: 

- https://youtu.be/6OokP-NE49k
- https://git-scm.com/

### Ciclo Arquivos no GIT 📁
 **Untracked => Unmodified => Modified => Staged => Commit**
 
 **Working Directory => Staging Area => Local Repository**
### Comandos de configuração 🛠️
 1. Altera o nome de usuário: `git config --global user.name nome`
 2. Altera o e-mail: `git config --global user.email email@gksa.com`
 3. Lista as configurações: `git config --list`

### Iniciando um repositório 💿
  1. Iniciar o GIT bash;
  2. Cria o repositório: `git init`
  3. Verifica se o repositório foi criado `ls -a`

### Primeiro commit 💾
 1. Seleciona os arquivos a serem adicionados `git add arquivo`
 2. Realiza o commit `git commit -m "mensagem"`

# Limpando commits 🧹 

 ### Tópicos ☑️ :

 - Mudar mensagem do commit:

   `git commit -m "mensagem" --amend  `  `git rebase -i HEAD~2`(lista os últimos commits iterativas)

 - Apagar commits mas sem perder as alterações dos commits:

   `git reset --soft HEAD~3`

 - Commitar arquivos de assuntos diferentes em commits diferentes:

   `git add -i`

   `git add -p "s"` (é possível escolher a linha da modificação de um mesmo arquivo em commits diferentes!)

 - Desfazer commits:

   `git reset --hard/soft HEAD~2` (Volta para o staged quando usamos o soft)

   `git checkout -b teste sha1` (Caso tenha feito alguma modificação hard em um arquivo que não gostaria)

 - `git bfg` (Reaponta as referências corretamente) _apenas paracasos extremos_
