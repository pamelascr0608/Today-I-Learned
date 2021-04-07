# Admin.py

```python
  from models import Produto , Cliente
  
  
  class ClienteAdmin(admin.ModelAdmin):
    list_display = ('name', )
    search_fields = ('name',)


admin.site.register(Cliente)

```
- Criar uma função str para nome (pode ser no models também):

```python
  def _str_(self)
    return f`({self.nome} {self.sobrenome})

```
<strong>Importante mudar a URL do admin no arquivo urls.py</strong>
