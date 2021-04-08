# Models.py

Arquivo que tem o modelo do banco de dados.
Mesmo se for clonado, sua configuração persiste no projeto, bastando criar o banco de dados e fazer as migrations.

<strong>QUEM TEM MODELS É A APLICAÇÃO!!!</strong>

```python
class Product(model.models):
  name= models.Charfield('Nome', max_lenght=100)
  price= models.DecimalField('Preço', decimal_places=2 , max_digits=8)
```
- Confirmar se a aplicação está no settings.py!
## Comandos para aplicar as modificações feitas nos models:
- Makemigrations cria a migration!
```cmd
python manage.py makemigrations
```
- Migrate executa a migration!
```cmd
python manage.py migrate
```
- SQL Migrate mostra instruções SQL para uma migração.
```cmd
python manage.py sqlmigrate
```
- Show migrations mostra a lista de migrations da aplicação e seu status.
```cmd
python manage.py showmigrations
```
<strong>⚠️ Para facilitar, tente pensar nas migrations como um versionamento do seu banco de dados. _makemigrations_ é responsável por "empacotar" suas mudanças em arquivos individuais, como um commit por exemplo. E _migrate_ aplica essas mudanças no banco de dados.</strong>
