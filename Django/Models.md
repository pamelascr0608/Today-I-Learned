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
- Makemigrations cria a migration!
```cmd
python manage.py makemigrations
```
- Migrate executa a migration!
```cmd
python manage.py migrate
```
