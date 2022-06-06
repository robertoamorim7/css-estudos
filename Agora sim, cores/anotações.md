# Cores
usamos CSS para alterar cores do nosso documento

## Tipos

-background-color (para caixas)
-color (para textos)
-border-color (para caixas)
-outros

## Valores
podemos definir os valores por

-palavra-chave (blue, red)
-hexadecimal(#990011)
-funções: rgb, rgba, hsl, hsla

```css
element {
    /* Keyword values*/
    color: currentcolor

    /*<named-color> values*/
    color: red;
    color: orange;
    
    /*<hex-color values> 0F*/
    color: #090
    color: #009900;
    color: #000a; /*o 'alpha' indica a transparência da cor*/
    color: 009900aa;

    /* <rgb()> values*/
    color: rgb(34, 12, 64, 0.6); /*0-255*/
    color: rgba(34, 12, 64, 0.6);
    color: rgb(34 12 64 / 0.6);
    color: rgba(34 12 64 /0.3);
    color: rgb(34. 0 12 / 60%);
    color: rgba(34.6 12 64 / 30%);

    /*<hsl()> values*/
    color: hsl(180, 100%, 50%, 60%); /* Hue - Saturation - Lumiance*/
    color: hsla(180, 100%, 50%, 60%);
    color: hsl(30 100% 50% / 0.6); 
    color: hsla(30 100% 50% / 0.6);
    color: hsl(30.0 100% 50% / 60%);
    color: hsla(30.2 100% 50% / 60%);

    /* Global values */
    color: inherit; /* Herda a cor do elemento anterior */
    color: initial; /* Volta a sua cor inicial */
    color: unset; /* Pega a cor do contexto */
}

```

Documentação: https://developer.mozilla.org/en-US/docs/Web/CSS/color_value
=========================================================================================

# Background
-Define um fundo para nosso elemento
-Sua área de atuação é a caixa toda
-Por padrão, é transparente

## exemplos
-Usar cores solidas
-Usar imagens
-Controlar
    -a posição das imagens
    -se elas se repetem ou não
    -o tamanho delas na caixa
-Usar cor e imagem juntas
-Usar cor gradiente

================================================================================================

## background-color

```css
* {
    margin: 0;
}

header {
    height: 100px;
    border: 7px dashed red;
    background-color: rgb(55, 100, 50);
}
```

```html
<header>

</header>
<main>
    <h1>Evolua rápido com a tecnologia</h1>
    <p>Junte-se a milhares de devs e acelere
    na direção dos seus objetivos</p>
</main>
```
================================================================================================
## background-image
-Para adicionar uma imagem como background podemos usar a propriedade background-image
-Por padrão a imagem vai se repetir e podemos modificar essa opção usando a propriedade background-repeat

```css
/** inserindo **/
background-image: url(endereço da imagem)
```
================================================================================================
## background-image-repeat

```css
/* Values */
background-repeat: repeat-x; /** repetir no eixo horizontal**/
background-repeat: repeat-y; /** repetir no eixo vertical**/
background-repeat: repeat;
background-repeat: space;
background-repeat: round;
background-repeat: no-repeat;

/* Podedmos usar 2 valores: horizontal | vertical */
background-repeat: repeat space;
background-repeat: repeat repeat;
background-repeat: round space;
background-repeat: no-repeat round;
```
================================================================================================

## background-position

-Com a propriedade background-position podemos mudar a posição da imagem do background.
```css
/* Pricipais valores */
background-position: top;
background-position: bottom;
background-position: left;
background-position: right;
background-position: center;
```
================================================================================================
## background-size
-Para mudar o tamanho da imagem do background usamos a propriedade background-size.

```css
/* Values */
background-size: cover;
background-size: contain;

/* Podemos usar 2 valores, o primeiro é para a largura da imagem e o segundo é para a altura */
background-size: 40% auto;
background-size: 2em 25%;
background-size: auto 8px;
background-size: auto auto;
```
================================================================================================

## background-origin-clip
-A propriedade background-origin é quem define o ponto de origem de uma imagem específica.

```css
/* Principais valores */
background-origin: border-box;
background-origin: padding-box;
background-origin: content-box;
```

-O background-clip define se a cor ou imagem do background iniciam debaixo de sua área de borda, preenchimento ou conteúdo.

```css
/* Principais valores */
background-clip: border-box;
background-clip: padding-box;
background-clip: content-box;
background-clip: text;
```
================================================================================================

## background-attachment
-A propriedade background-attachment determina se a posição da imagem vai ser fixa ou se vai rolar junto com o conteúdo.

```css
/* Principais valores */
background-attachment: scroll; /** padrao **/
background-attachment: fixed;
background-attachment: local;
```
================================================================================================

## background:linear-gradient
-linear-gradient() é a função usada para criar gradient linear com o CSS.

```css
background: linear-gradient(45deg, red, yellow)
```

-radial-gradient() é a função usada para criar gradient circular.

```css
background: radial-gradient(green, red, yellow)
background: radial-gradient(rgba(255, 255, 255, 0), rgba(255, 0, 0, 0.2))
```

## multiplos valores
-Podemos aplicar múltiplos backgrounds em um mesmo elemento, podendo ter cor sólida, gradiente ou imagem. Para isso basta separar por vírgula cada background.