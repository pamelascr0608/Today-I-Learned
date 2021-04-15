# Como conectar em um servidor

1. Ter usuário e IP do server;
2. Abrir o Putty;
3. Digitar em host name: user@ipserver (Ex.: root@123.45.67.8);
4. Open;
5. Colocar a senha do servidor.

# Ativar a virtualenv

1. Ir até a pasta de virtualenv projeto (Ex.:  /home/virtualenvs/PROJETO/bin/activate);
2. <code>source  /home/virtualenvs/PROJETO/bin/activate</code>;

# Atualizar o conteúdo

1. Ir até a pasta do projeto;
2. <code> cd /home/webapps/PROJETO</code>;
3. <code> git pull</code>;
4. Se necessário, rodar migrate, collectstatic ou fixtures: <br>
<code>  python manage.py migrate</code> <br>
<code>  python manage.py collectstatic </code> <br>
<code>  python manage.py loaddata path_fixture </code> <br>

### Caso tenha arquivos media:

1. Conectar no servidor usando o Filezilla e SFTP (usar credenciais do Putty);

# Para reiniciar a aplicação:

_No servidor LaraTech:_
<code>python manage.py runserver</code>

_Em servidores oficiais:_
<code>sudo systemctl restart gunicorn</code>
