# Layout e evolução

Layout tem a ver com a maneira que os elementos estão distribuídos na tela

## Normal flow

Ou flow layout, é a maneira que os elementos `block` e `inline` ficam na página

```html
<p> Texto block com <strong>inline</strong> dentro </p>
```

## Tables

É a maneira de tabelas onde a tag `table` recebe um display `table` fazendo com que os elementos internos como `td` e `tr` possam ser usados para montar uma tabela

## Tableless

Uso de propriedades `float` e `clear` para que os elementos possam mudar de posição na tela

```html
<div style="float:left">
</div>

<div style="float:right"> 
</div>
<div style="clear:both">
</div>
```

## Flexbox

A caixa se torna flex, fazendo com que seus elementos internos possam receber melhor:
- alinhamento
- ordenação
- tamanhos flexíveis

```html
<div class="flexbox">
  <div class="item">Cachorro</div>
  <div class="item">Macaco</div>
  <div class="item">Papagaio</div>
</div>
```
```css
.flexbox {
  display: flex;
}
```

=========================================================

# Terminologia

Flex container
    - flex item

Nesting
Axis
    - main
        start, end
    - cross
        star, end

Flex sizing
    - flexível
    - altera width/height dos itens para preenchimento dos espaços do flex container

======================================================

# Propriedades do flex container

Direção dos itens
Multi linhas
Alinhamento
    principal
    cruzado
Espaço entre os itens

# Direção dos itens

Flex é uma dimensão (horizontal ou vertical)
Podemos mudar a direção com `flex-direction`
Valores: (row | row-reverse | column | column-reverse)

# flex-wrap

- Podemos usar multi linhas
- Cada nova linha possui um novo flex container
    - cria novas linhas somente se for necessário

# flex-flow

- shorthand
- flex-direction || flex-wrap

```css
.box {
    display: flex;
    flex-flow: column wrap;
}
```

# justify-content

- alinhamento dos elementos dentro do container
- distribuição dos elementos

## valores

- flex-start
- flex-end
- center
- space-around
- space-between
- space-evenly

# align-itens

- alinhamento dos elementos no eixo cruzado

## valores

- strech
- flex-start
- flex-end
- center

# gap

- espaço entre os elementos

## valores

Unidades de medida
fixas: px, pt
flexíveis: %, em, rem

==========================================================

# Propriedaes para os itens

- flex-basis
    aumenta o tamanho do conteúdo

- flex-grow
    crescimento do item dentro do container em relaçao aos espaços vazios

- flex-shrink
    encolher o item dentro do container

- flex
    shorthand
    flex-grow flex-shrink flex-basis
    podem ter 1-3 valores

- order
    ordenar elementos dentro de uma caixa
    padrao: 0

