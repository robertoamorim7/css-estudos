# Comentarios
-não irá afetar seu codigo
-ajuda a lembrar blcos de codigos
-deixa dicas para leitura
-ajuda outros a entenderem
-nunca esqueça de fechar um comentário aberto

Comentários começam com '/*' e terminam com '*/'

-Voce pode usar comentarios para desabilitar partes do seu codigo

# CODIGOS FORAM FEITOS NO CODEPEN

----------------------------------------------------------------------------------------------

# Anatomia

```css
h1 {
    color: blue;
    font-size: 60px;
    background: gray;
}
```
-selector: (h1) procura no html alguma tag h1, e a todas serao aplicadas estas propriedades.
-declaration: todas as alterações
-properties: "color"
-property value: "blue"
 
-----------------------------------------------------------------------------------------------

# Seletores
Conecta um elemento html com o CSS

## Tipos
-Global selector: '*'
-Element/type selector: 'h1, h2, p, div'
-ID selector: '#box, #container'
-class selector: '.red, .m-4'
-attribute selector. pseudo-class, pseudo-element, e outros 

```html
<div id="container" class="m-40">
  <h1>Título</h1>
  <h2>Subtitulo</h2>  
</div>
```

```css
* {
  margin: 0;
  
}

#container {
  width: 200px;
}

.m-40 {
  margin: 40px;
}
h1,h2 {
    color: white;
    font-size: 50px;
    background: black;
}
```

--------------------------------------------------------------------------

# Box Model

-voce ira perceber que (quase) tudo sao caixas no CSS
-posicionamemntos, tamanhos, espaçamentos, bordas, cores
-caixa pode ficar ao lado uma da outra, ou acima
-elementos html sao caixas

```html
<h1>Evolua Rapido</h1>
<p>Descrição</p>
<button>Embarcar</button>
```
```css
h1 {
  border: 2px solid red;
  margin: 20px;
  padding: 20px;
  
}
```
---------------------------------------------------------------------------------

# Adicionando CSS em um doc html

## inline
-atributo 'style' aplicado diretamente na tag do html

## <style>
-tag html que irá conter o css e fica dentro do head

## <link>
-arquivo css externo

## @import
-arquivo css externo

------------------------------------------------------------------------------

# A cascata (cascading)

A escolha do browser de qual regra aplicar, caso haja muitas para o mesmo elemento.
-seu estilo é lido de cima para baixo.

É levado em consideração 3 fatores
1. origem do estilo
2. especificidade
3. importancia

### Oirgem do estilo
inline > tag style > tag link

### Especificidade
É um cálculo matemático onde cada tipo de seletor e origem do estilo possuem valores a serem considerados.

0. Universal selector, combinators e negation pseudo-class (:not())
1. Element type selector e pseudo-elements (::before, ::after)
10. Classes e attribute selectors ([type="radiio"])
100. ID selector
1000. inline

----------------------------------------------------------------------------------------------------

### A regra !important
-cuidado, evite o uso
-não é considerado uma boa prática
-quebra o fluxo natural da cascata
*faz com que aquele comando quebre todas as regras da cascata e sobrescreva as estilzações 

```css
h1 {
    color: blue !important;
}
```
-----------------------------------------------------------------------------------------------------

# At-rule
-está relacionado ao comportamento do CSS
-começa com o sinal '@' seguido do identificador e valor

## Exemplos comuns

- @import    /* incluir um CSS externo */
- @media     /* regras condicionais para dispositivos */
- @font-face /* fontes externas */
- @keyframes /* Animation */

```css
@import "https://local.com/style.css";

@media (min-width: 500px) {
    /* rules here*/
}

@fonte-face {
    /* rules here*/
}

@keyframes nameofanimation {
    /* rules here*/
}
```

-----------------------------------------------------------------------------------------------

# Shorthand
-junção de propriedades
-resumido
-legível

```css
{
    /*background properties*/
    background-color: #000;
    background-image: url(images/bg.gif);
    background-repeat: no-repeat;
    background-position: left top;

    /* background shorthand*/
    background: #000 url(images/bg.gif) no-repeat left top;

    /* font properties */
    font-style: italic;
    font-weight: bold;
    font-size: .8em;
    line-height: 1.2;
    font-family: Arial, sans-serif;

    /* font shorthand */ 
    font: bold italic .8em/1.2 Arial, sans-serif;
}
```

## Detalhes
-nao ira considerar propriedades anteriores
-valores nao especificados irão assumir o valor padrão
-geralmente a ordem descrita não importa, mas se houver muitas propridades com valores semelhantes, poderemos encontrar problemas.

## Propriedades que aceitam shorthand
**https://developer.mozilla.org/pt-BR/docs/Web/CSS/Shorthand_properties**

---------------------------------------------------------------------------------------------------------

# Funções
-nome seguido de abre e fecha parenteses
-recebe argumentos

## Exemplos

```css
@import url("https://urlaqui.com/style.css")

{
    color: rgb(255, 0, 100);
    width: calc(100% - 10px)
}
```
----------------------------------------------------------------------------------------------------------

# DevTools
-apertando f12 no browser acessamos o devtools

# Cuidados com a escrita
-É importante prestar atenção à sua escrita do CSS, identar seu código para facilitar a leitura, e mais importante, manter tudo organizado e funcionando!

# Vendeor prefixes
-São coisas que permitem que browsers adiocionem features a fim de colocar em uso alguma novidade que vemos no CSS.

Exemplos:
```css
p {
	-webkit-background-clip: text; /*Chrome, Safari, iOS e Android*/
	-moz-background-clip: text; /* Mozilla (Firefox) */
	-ms-background-clip: text; /* Internet Explorer ou Edge*/
	-o-background-clip: text; /* Opera */
Você também pode consultar se a feature pode ser utilizada através dos sites:
```
https://ireade.github.io/which-vendor-prefix

https://caniuse.com