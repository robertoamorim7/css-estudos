# Seletores

Conecta um elemento HTML com o CSS a fim de alterar o elemento

## Tipos

Element selector
    - todos os elementos html
    ex: p {}
    
ID selector
    - um elemento que tenha o atributo `id`
    - cada id deverá ser único
    ex: #content

Class selector
    - os elementos que contenham um atributo `class`
    - podemos ter uma ou mais classes
    ex: .class

Attribute selector
    - um elemento que tenha um atributo específico
    ex: [title]

Pseudo-class selector
    - elementos em um estado específico
    p:hover {
        color: red
    }

## Multiplos

Voce poderá selecionar multiplos elementos e aplicar alguma regra css para todos eles
Usamos a separação por virgulas

```css
h1, p, a, .red {
    color: red;
}
```

# Combinators

Combinadores, pois eles trabalham para buscar e combinar seletores a fim de aplicar uma estilização

## Descendant combinator

- identificado por um espaço entre os seletores
- busca um elemento dentro de outro
```css
body article h2 {
    color: red
}
```

## Child combinator

- identificado pelo sinal ` > ` entre dois seletores
- seleciona somente o elemeto que é filho direto do pai

```css
body > ul > li {
    color: blue;
}
```

## Adjacent sibling combinator

- identificado pelo sinal ` + ` entre dois seletores
- seleciona somente o elemento do lado direto que é irmaõ direto na hierarquia

```css
h1 + p
```

## General sibling combinator

- identificado pelo sinal ` ~ ` entre dois seletores
- seleciona todos os elementos

```css
h1 ~ p
```

## Utilizando combinators

```css
ul > li[class="red"]
```

============================================================================

# Pseudo-classes

É um tipo de seletor que irá selecionar um elemento que estiver em um estado específico
Ex: é o primeiro elemento dentro de uma caixa caixa, ou o elemetno está com o ponteiro do mouse em cima dele

Pseudo classes começam com dois pontos seguidos do nome da pseudo classe `:pseude-class-name`

## Selecionando elementos com a pseudo-classe

- `:first-child` seleciona primeiro elemento do pai
- `:nth-of-type()` seleciona o elemento do tipo da tag
- `:nth-child()` seleciona o elemento selecionado do elemento pai
- `:nth-child(even/odd)` seleciona todos os elementos pares ou ímpares do pai

# Ações do usuário

- `:hover` seleciona uma condição para quando o usuário passar o mouse em cima do elemento
- `:focus` para campos de texto, seleciona condição para quando o usuário selecionar a caixa de texto

## Atributos

- `:disabled`
- `:required`

==========================================================================

# Pseudo-elements

Com pseudo-elements nós podemos adicionar elementos HTML pelo próprio CSS

`::pseudo-element-name`

## Exemplos

- `::before`
- `::after`
- `::first-line`

```css
    li:before {
        content: "";
        width: 10px;
    }
```
