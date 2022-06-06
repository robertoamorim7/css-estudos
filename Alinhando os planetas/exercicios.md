1)
```html
    <header>
  <nav>
    <a href="#">LOGO</a>
    <ul>
      <li>HOME</li>
      <li>ABOUT</li>
      <li>SERVICES</li>
      <li>TESTIMONIALS</li>
      <li>CONTACT</li>
    </ul>
  </nav>
</header>
```
```css
    * {
  margin: 0;
}
header {
  padding: 4rem;
  background: lightgray;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  
}

ul {
  display: flex;
  list-style: none;
  gap: 0.8rem;
  align-items: center;
}

ul li:last-child {
  background: black;
  color: white;
  padding: 0.8rem;
}
```
==============================================

2)
```html
    <div class="container">
    <aside>Coluna esquerda</aside>
    <main>Coluna direita</main>
    </div>
```

```css
    .container {
      display: flex;
      gap: 1rem;
    }

aside, main {
  border: 1px solid;
  height: 95vh;
}

aside {
  flex-basis: 25%;
}

main {
  flex: 1;
}
```
==================================================

3)
```html
    <div class="container">
  <img src="https://source.unsplash.com/random" alt="">
  <img src="https://source.unsplash.com/random" alt="">
  <img src="https://source.unsplash.com/random" alt="">
  <img src="https://source.unsplash.com/random" alt="">
  <img src="https://source.unsplash.com/random" alt="">
  <img src="https://source.unsplash.com/random" alt="">
  <img src="https://source.unsplash.com/random" alt="">
  <img src="https://source.unsplash.com/random" alt="">
  <img src="https://source.unsplash.com/random" alt="">
</div>
```
```css
img {
  width: 30%;
  height: 30%;
}

.container {
  display: flex;
  flex-wrap: wrap;
  gap: .8rem;
  justify-content: center;
}
```
=================================================
4)
```html
<button>
  <img id="cart" src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiA/PjxzdmcgYmFzZVByb2ZpbGU9InRpbnkiIGhlaWdodD0iMjRweCIgdmVyc2lvbj0iMS4yIiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNHB4IiB4bWw6c3BhY2U9InByZXNlcnZlIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIj48ZyBpZD0iTGF5ZXJfMSI+PGc+PHBhdGggZD0iTTIwLjc1Niw1LjM0NUMyMC41NjUsNS4xMjYsMjAuMjksNSwyMCw1SDYuMTgxTDUuOTg2LDMuODM2QzUuOTA2LDMuMzU0LDUuNDg5LDMsNSwzSDIuNzVjLTAuNTUzLDAtMSwwLjQ0Ny0xLDEgICAgczAuNDQ3LDEsMSwxaDEuNDAzbDEuODYsMTEuMTY0YzAuMDA4LDAuMDQ1LDAuMDMxLDAuMDgyLDAuMDQ1LDAuMTI0YzAuMDE2LDAuMDUzLDAuMDI5LDAuMTAzLDAuMDU0LDAuMTUxICAgIGMwLjAzMiwwLjA2NiwwLjA3NSwwLjEyMiwwLjEyLDAuMTc5YzAuMDMxLDAuMDM5LDAuMDU5LDAuMDc4LDAuMDk1LDAuMTEyYzAuMDU4LDAuMDU0LDAuMTI1LDAuMDkyLDAuMTkzLDAuMTMgICAgYzAuMDM4LDAuMDIxLDAuMDcxLDAuMDQ5LDAuMTEyLDAuMDY1QzYuNzQ4LDE2Ljk3Miw2Ljg3LDE3LDYuOTk5LDE3QzcsMTcsMTgsMTcsMTgsMTdjMC41NTMsMCwxLTAuNDQ3LDEtMXMtMC40NDctMS0xLTFINy44NDcgICAgbC0wLjE2Ni0xSDE5YzAuNDk4LDAsMC45Mi0wLjM2NiwwLjk5LTAuODU4bDEtN0MyMS4wMzEsNS44NTQsMjAuOTQ1LDUuNTYzLDIwLjc1Niw1LjM0NXogTTE4Ljg0Nyw3bC0wLjI4NSwySDE1VjdIMTguODQ3eiBNMTQsNyAgICB2MmgtM1Y3SDE0eiBNMTQsMTB2MmgtM3YtMkgxNHogTTEwLDd2Mkg3QzYuOTQ3LDksNi44OTksOS4wMTUsNi44NTIsOS4wM0w2LjUxNCw3SDEweiBNNy4wMTQsMTBIMTB2Mkg3LjM0N0w3LjAxNCwxMHogTTE1LDEydi0yICAgIGgzLjQxOGwtMC4yODUsMkgxNXoiLz48Y2lyY2xlIGN4PSI4LjUiIGN5PSIxOS41IiByPSIxLjUiLz48Y2lyY2xlIGN4PSIxNy41IiBjeT0iMTkuNSIgcj0iMS41Ii8+PC9nPjwvZz48L3N2Zz4=" alt="">
  Comprar
</button>
```

```css
button {
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  background: purple;
  width: 200px;
  height: 60px;
  font-size: 1.4rem;
  gap: 0.4rem;
  border-radius: 4px;
}

button img {
  width: 2rem;
  height: 2rem;
}

```
============================================================

5)
```html
<footer class="footer">
    Footer
</footer>
```

```css
    * {
  margin: 0;
}

body {
  min-height: 100vh;
  display: flex;
}

footer {
  margin-top: auto;
  font-size: 3rem;
  background: grey;
  color: white;
  height: 8rem;
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  
  
}
```