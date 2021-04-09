# Models.py

Arquivo que tem o modelo do banco de dados.
Mesmo se for clonado, sua configuração persiste no projeto, bastando criar o banco de dados e fazer as migrations.

<strong>QUEM TEM MODELS É A APLICAÇÃO!!!</strong>

```python
class Product(model.models):
  name= models.Charfield('Nome', max_lenght=100)
  price= models.DecimalField('Preço', decimal_places=2 , max_digits=8)
```
- _class_: Indica que estamos definindo um objeto;
- _Product_: Indica o nome do modelo (Sempre em maiúisculo).
- _models.Model_: O objeto é um modelo do Django, então indica que ele será salvo no banco de dados.
- Confirmar se a aplicação está no settings.py!

### Outros modelos:
<code>models.ForeignKey</code> : Link para outro modelo já existente. Ex.: <code>Ex.: example = models.ForeignKey(settings.AUTH_USER_MODEL, on_delete = models.CASCADE)</code><br>
<code>models.CharField</code>: Texto com caracteres limitados (como no exemplo acima); <br>
<code>models.TextField</code>: Texto sem um limite fixo. Ex.: <code>example = models.TextField()</code> <br>
<code>models.DateTimeField</code> : Inclui data e hora no modelo. Ex.: <code>example = modelsDateTimeField(default=timezone.now)</code> <br>


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


## Referências: 

- https://tutorial.djangogirls.org/pt/django_models/
