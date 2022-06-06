# Valores e unidades de medida
-cada propriedade possui valores `property: value`
-estudo constante a fim de entender as propriedades e seus valores

## Prática
-como conheer e estudar os valores na documentação?
    * <color> <length>
-os termos podem variar. `values` ou `data types`

========================================================================

# Tipos numéricos
-<integer> - número inteiro como -10 ou 223
-<number> - número decimal como -2.4, 64 ou 0.234
-<dimension> - é um <number> com uma unidade junto: 90deg, 2s, 8px
-<percentage> - representa uma fração de outro número: 50%

## Unidades comuns
-<length> - é um dos mais usados no CSS e representa um valor de distância: px, em, vw
-<angle> - representa um ângulo: deg, rad, turn
-<time> - representa um tempo: s, ms
-<resolution> - representa resoluções para dispositivos: dpi

=========================================================================

# Distâncias absolutas <length>

São fixas e não alteram seu valor.
Unidade       Nome                   Equivalência
cm            Centímetros            1cm = 96px/2.54
in            inches(polegadas)      1in = 2.54cm = 96px
px            Pixels                 1px = 1/96th of 1in

-o mais comum e mais utilizado é o **px**
-nao recomendado usar em cm

# Distâncias relativas

São relativas a algum outro valor, pode ser o elemento pai, ou root, ou o tamanho da tela.
-beneficio: maior adaptação aos diferentes tipos de tela
Unidade     Relativo a
em          Tamanho da fonte do pai
rem         Tamanho da fonte do elemento raiz (root/html)
vw          1% da viewport width
vh          1% da viewport height

=============================================================================

# Porcentagens %
-em muitos casos é tratado da mesma maneira que as distâncias <lenght>
-sempre será relativo a algum valor
<ul>
	<li>One</li>
	<li>Two</li>
	<li>Three
		<ul>
			<li>Three A</li>
			<li>Three B</li>
			<ul>
				<li>Three B 2</li>
			</ul>
		</ul>
	</li>
</ul>
li {
    font-size: 80%;
}

==============================================================================

# Position
<position>

Representa um conjunto de coordenadas 2D:
-top, right. bottom. left e center

-usados para alguns tipos de propriedades
-não confundir com a propriedade `position`

=============================================================================

# Funções
-em programação, funções são conhecidas por causar um reaproveitamento de código

* rgb()
* hsl()
* url ()
* calc ()

========================================================================

# Strings e identificadores
-strings: texto envolto em aspas
-identificadores: red, black, gold, etc.
```css
.box::after {
	content: "Isso é uma string"
}
```