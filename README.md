# Portfólio - HTML e CSS

Este projeto foi desenvolvido durante o **Programa ONE (Oracle Next Education)**, resultado da parceria entre a **Oracle** e a **Alura**.  
Trata-se de um exercício prático do curso de **HTML e CSS**, com foco especial na **organização do CSS** e no **uso de variáveis** para garantir consistência visual e facilidade de manutenção.

---

## 📁 Estrutura do projeto
- `index.html` — Página principal (apresentação, links para redes).  
- `about.html` — Página "Sobre mim".  
- `styles/style.css` — Arquivo de estilos (centraliza cores, fontes e layout).  
- `assets/` — Imagens e ícones usados (ex.: `imagem.png`, `github.png`, `linkedin.png`, `twitch.png`).

---

## 🎯 Principais pontos (foco em CSS e variáveis)
O diferencial deste projeto é o **uso de variáveis CSS** (declaradas em `:root`) para centralizar cores, tipografia e espaçamentos. Isso facilita alterar a identidade visual sem ter que modificar regras dispersas pelo arquivo.

### Exemplo de variáveis (coloque no início de `styles/style.css`)
```css
:root {
  /* --- Cores --- */
  --cor-primaria: #000000;     /* cor dos textos principais / títulos */
  --cor-secundaria: #F6F6F6;   /* fundo geral */
  --cor-destaque: #22D4FD;     /* cor para links/hover/destaques */
  --cor-hover: #272727;        /* cor alternativa para estados hover */

  /* --- Tipografia --- */
  --fonte-titulo: 'Krona One', sans-serif;
  --fonte-texto: 'Montserrat', sans-serif;

  /* --- Espaçamento / Layout --- */
  --gap-horizontal: 1.6rem;
  --largura-max: 1100px;
  --radius-card: 12px;
}
```

### Como essas variáveis são usadas (exemplos)
```css
body {
  font-family: var(--fonte-texto);
  background-color: var(--cor-secundaria);
  color: var(--cor-primaria);
  line-height: 1.6;
}

.cabecalho {
  display: flex;
  justify-content: center;
  padding: 1.2rem;
  background: var(--cor-primaria);
  color: var(--cor-secundaria);
}

.apresentacao__conteudo__titulo {
  font-family: var(--fonte-titulo);
  color: var(--cor-primaria);
}

.apresentacao__links__link:hover {
  color: var(--cor-destaque);
  transform: translateY(-2px);
}
```

---

## 🧩 Classes e organização (baseado nos seus HTMLs)
As páginas já usam um padrão BEM-like que facilita componentização:
- `.cabecalho`, `.cabecalho__menu`, `.cabecalho__menu__link`  
- `.apresentacao`, `.apresentacao__conteudo`, `.apresentacao__conteudo__titulo`, `.apresentacao__conteudo__texto`  
- `.apresentacao__links`, `.apresentacao__links__link`, `.titulo-destaque`  
- `.rodape`

Recomendações:
- Estilize por escopo (ex.: `.apresentacao__conteudo { ... }`) para evitar vazamento de estilos.  
- Use variáveis para cores, fontes e gaps — assim qualquer ajuste de identidade visual é rápido.

---

## ✅ Boas práticas aplicadas / recomendadas
- Centralize variáveis no `:root` (cores, fontes, medidas).  
- Separe regras globais (reset, tipografia) de regras de componentes.  
- Use unidades relativas (`rem`, `%`) para responsividade.  
- Adote `max-width` e `margin: 0 auto` para centralizar o container (`--largura-max`).  
- Use media queries (ex.: `@media (max-width: 768px)`) para empilhar elementos em telas pequenas.  
- Otimize imagens em `assets/` (tamanho e formato).

---

## 🛠 Testar localmente
1. Abra `index.html` no navegador (funciona sem servidor).  
2. Para servir localmente (opcional), execute:
```bash
# com Python 3
python -m http.server 8000
# abra http://localhost:8000 no navegador
```

---

## 📌 Observações finais
- O README enfatiza que o foco do projeto é o **CSS** bem organizado e o uso de **variáveis**.  
- Se quiser, posso:
  - Gerar um `styles/style.css` completo de exemplo baseado nas classes do seu HTML; ou  
  - Ler o seu `styles/style.css` (se enviar) e extrair as variáveis reais para documentá-las aqui.

---

## 🏷 Créditos
Projeto desenvolvido durante o curso **HTML e CSS** da **Alura**, dentro do **Programa ONE — Oracle Next Education**.

---

![Preview do projeto](./assets/imagem.png)
