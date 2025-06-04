
# Aula Completa: HTML + CSS na Fazendinha CSS

## Início da Aula: O que vamos aprender?
**Objetivo**: Fazer uma página HTML e estilizar totalmente usando CSS.

**Conteúdos esperados**:
- Estrutura básica HTML
- Elementos principais (`div`, `img`, `p`, `h1`, `span`)
- Atributos (`id`, `class`, `alt`, `href`)
- CSS externo, interno e inline
- Seletores CSS
- Box model
- Propriedades visuais (`color`, `background`, `border`, `padding`, `margin`, etc.)
- Positioning
- Flexbox e Grid (básico)
- Animações e transições
- Responsividade
- Pseudo-elementos e pseudo-classes

Vamos aprender **tudo isso** criando a fazendinha!

---

## Estrutura HTML básica

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Fazendinha CSS</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Bem-vindo à Fazendinha CSS 🐄🌻</h1>
  <div class="sky"></div>
  <div class="field"></div>
  <div class="cow"></div>
</body>
</html>
```

**Conceitos**:
- Estrutura HTML básica
- Tag `<link>` para CSS externo
- Divisão com `<div>`
- Título com `<h1>`

---

## Primeiros estilos CSS: Céu e Campo

```css
body {
  margin: 0;
  padding: 0;
  font-family: sans-serif;
  text-align: center;
}

.sky {
  width: 100%;
  height: 50vh;
  background: linear-gradient(to bottom, #87ceeb, #add8e6);
}

.field {
  width: 100%;
  height: 50vh;
  background-color: #7cfc00;
}
```

**Conceitos**:
- `margin`, `padding`, `font-family`
- `width`, `height`, `background`, `linear-gradient`
- Unidades relativas (`vh`, `%`)

---

## A Vaca Aparece!

```html
<div class="cow"></div>
```

```css
.cow {
  width: 100px;
  height: 60px;
  background-color: white;
  border: 2px solid black;
  border-radius: 20px;
  position: absolute;
  bottom: 10vh;
  left: 10vw;
}
```

**Conceitos**:
- `border`, `border-radius`
- `position: absolute`

---

## Imagens e Texto

```html
<div class="cow">
  <img src="https://placekitten.com/100/60" alt="Vaquinha">
  <p>Mimosa 🐮</p>
</div>
```

```css
.cow img {
  width: 100%;
  height: auto;
  border-radius: 20px;
}

.cow p {
  margin: 5px 0 0;
  font-weight: bold;
}
```

**Conceitos**:
- Uso de `<img>`, `alt`
- Texto com `<p>`, propriedades de fonte

---

## Manchinhas com Pseudo-elementos

```css
.cow::before, .cow::after {
  content: '';
  width: 20px;
  height: 20px;
  background: black;
  border-radius: 50%;
  position: absolute;
}

.cow::before {
  top: 10px;
  left: 10px;
}

.cow::after {
  top: 30px;
  left: 60px;
}
```

**Conceitos**:
- Pseudo-elementos `::before`, `::after`

---

## Movimento e Animação

```css
@keyframes moveCow {
  0% { left: 10vw; }
  50% { left: 70vw; }
  100% { left: 10vw; }
}

.cow {
  animation: moveCow 8s infinite linear;
}
```

**Conceitos**:
- `@keyframes`
- `animation`

---

## Flexbox para Centralizar

```css
body {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
```

**Conceitos**:
- Flexbox básico

---

## Adicionando um Sol

```html
<div class="sun"></div>
```

```css
.sun {
  width: 80px;
  height: 80px;
  background: yellow;
  border-radius: 50%;
  position: absolute;
  top: 20px;
  right: 20px;
  box-shadow: 0 0 20px yellow;
  animation: spinSun 10s linear infinite;
}

@keyframes spinSun {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
```

**Conceitos**:
- `box-shadow`
- `transform: rotate`

---

## Responsividade (Media Queries)

```css
@media (max-width: 600px) {
  .cow {
    width: 70px;
    height: 40px;
  }

  .sun {
    width: 50px;
    height: 50px;
  }
}
```

**Conceitos**:
- `@media` queries para responsividade

---

## Resumo Geral

- Estrutura básica do HTML
- Divs e Containers
- Seletores e Estilização no CSS
- Box Model e Posicionamento
- Animações e Transições
- Flexbox básico
- Responsividade
- Pseudo-elementos

---

**Fim da Aula!**
