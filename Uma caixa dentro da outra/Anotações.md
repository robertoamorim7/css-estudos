# Box Model
-fundamental para fazer layouts para a web
-maior facilidade para aplicar o css

## o que é?
-uma caixa retangular
-essa caixa possui propriedades de uma caixa (2d)

-tamanho (largura x altura)    width | height
-conteúdo                      content
-bordas                        border
-preenchimento interno         padding
-espaços fora da caixa         margin

**Cada elemento na sua pagina será considerado uma caixa**

## box sizing
Como será calculado o tamanho total da caixa?
- content-box | border-box

```css
* {
    box-sizing: border-box
}

div {
    box-sizing: border-box; /** calcular o tamanho da caixa com base na borda e não do conteúdo  **/
}
```
=======================================================================================================


# Display: block vs display: inline
-como as caixas se comportam em relação as outras caixas
-comportamento externo das caixas
-os elementos sao inline por padrao
**block**                             **inline**
-ocupa toda a linha colocando          -elemento ao lado do outro
o proximo elemento abaixo desse
-width e height sao respeitados        -width e height nao sao funcionam
-padding, margin, border irao          -somente valores horizontais de margin, padding e border
funcionar normalmente.

ex:
block: `<p> <div> <section>`, todos os headings `<h1><h2>...`
inline: `<a><strong><span><<em>`
==========================================================================================================

## margin
Espaços entre os elementos
- margin-top | margin-rigth | margin-bottom | margin-left
- values: `<length>` | `<percentage>` | auto

Geralmente usamos uma forma abreviada (shorthand) para escrever o margin. Esse formato segue o sentido horário iniciando pelo top, seguindo para right, bottom e left.

```css
div {
    margin: 12px 16px 10px 4px; /* TOP = 12px | RIGHT = 16px | BOTTOM = 10px | LEFT = 4px */
    margin: 12px 16px 0; /* TOP = 12px | RIGHT = 16px | BOTTOM = 0px | LEFT = 16px */
    margin: 8px 16px; /* TOP = 8px | RIGHT = 16px | BOTTOM = 8px | LEFT = 16px */
    margin: 8px; /* TOP = 8px | RIGHT = 8px | BOTTOM = 8px | LEFT = 8px */
}
```
-cuidado com o margin collapsing (top se junta ao bottom)
===========================================================================================================
## padding
Preenchimento interno da caixa
-padding-top | padding-right | padding-bottom | padding-left
- values: `<length>` | `<percentage>`

padding: 12px 16px 10px 4px; /* TOP = 12px | RIGHT = 16px | BOTTOM = 10px | LEFT = 4px */
padding: 12px 16px 0; /* TOP = 12px | RIGHT = 16px | BOTTOM = 0px | LEFT = 16px */
padding: 8px 16px; /* TOP = 8px | RIGHT = 16px | BOTTOM = 8px | LEFT = 16px */
padding: 8px; /* TOP = 8px | RIGHT = 8px | BOTTOM = 8px | LEFT = 8px */


=========================================================

## border (e outline)
as bordas da caixa

Documentação do MDN: https://developer.mozilla.org/en-US/docs/Web/CSS/border

- value: <border-style> | <border-width> | <border-color>
- width: <length>
- color: <color>

por regra o tamanho da caixa se soma ao tamanho da borda, para evitar deve ser feito o border-box: box-sizing

```css
div {
	/* shorthand */
	border-top: solid 2px; /* top | right | bottom | left */

	/* style */
	border: solid;

	/* width <length> | style */
	border: 2px dotted;

	/* style | color */
	border: outset #f33;

	/* width | style | color */
	border: medium dashed green;

}
```
## outline
-O outline é muito semelhante ao border, mas difere em 4 sentidos:
    -Não modifica o tamanho da caixa, pois não é parte do Box Model
    -Poderá ser diferente de retangular
    -Não permite ajuste individuais
    -Mais usado pelo user agent para acessibilidade