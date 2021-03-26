# Funções dos arquivos no Django

<p>Primeiramente, é preciso pontuar a diferença de um projeto para uma aplicação nesse framework Python.<br>
O projeto engloba o todo, enquanto as aplicações são plugáveis. Desse modo, um projeto pode ter mais de uma aplicação.</p>

## O padrão MTV
É um padrão de projeto que pode ser analisado na imagem a seguir: 

![image](https://user-images.githubusercontent.com/78767309/112556209-74e32f00-8da8-11eb-834e-32980b093c79.png)

Ao fazermos uma solicitação (request) para o browser, ela "procura" a URL desejada, que encaminha para as views,models e database, respectivamente.
Após chegar no database, ela retorna pelo mesmo caminho, configurando assim o padrão M _(models)_ , T _(templates)_ , V _(views)_ .

## Arquivos de um projeto 

<h3>settings.py :</h3> Apresenta as principais configuraões do projeto, como banco de dados, templates, middlewares e apps instalados.
<h3>views.py :</h3> As views ficam dentro das aplicações. 

```py
def index(request)
  return render(request, 'index.html')
```

É uma função que recebe a variável request e retorna uma página (render).

<h3>urls.py :</h3> Criam rotas específicas para cada view. 

```py
path('', nome_view.home name='home')
```
