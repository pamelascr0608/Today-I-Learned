# CSS Responsivo 📱

## Grid:
- Divide a página em linhas e colunas;
- Coloca elementos em qualquer posição;
- Bidimensional.

## FlexBox:
- Unidimensional;
- Complementa o trabalho do grid.

## Propriedades:
  ### 1. Container:
 
    - display: grid (Define o container como grid);
    - grid-template-columns (Fatia o grid em colunas);
    - grid-template-rows (Fatia o grid em linhas);
    - grid-gap (Espaçamento);
    -- grid-row-gap;
    -- gri-column-gap;
    - grid-template-areas (Delimita áreas);
    
  ### 2. Item:
 
    - grid-column;
    -- grid-column-start;
    -- grid-column-end;e ai
    - grid-row;
    -- grid-row-start;
    -- grid-row-end;
    - grid-area (Nome no grid-template-areas)
      
## CSS Unitis
- Fixo:
  1. Pixels - px
- Fluido:
  1. Porcentagem - %
  2. Automática - auto
  3. Viewport Height - vh (100vh - toda parte visível da tela)
  4. Viewport Width - vw
 
 ### - Textos fixos:
  1. Pixels - px
- Textos responsivos:
  1. "Em" - multiplicado pelo elemento pai
  2. "Rem" - multiplicado pelo rootdo navegador


### Media queries

``` CSS
@media (max-width:768px){
}


@media only screen and (max-width:550px){ ... }
```

#### Observações:
```
grid-template-columns: repeat(auto-fit, minmax(250), 1fr) // Ajusta as colunas de acordo com a largura estabelecida (min 250px max 1fr)
```
