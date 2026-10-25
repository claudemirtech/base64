<div align="center">

# AtomicWeb - Base64

**Decodificador e visualizador de arquivos Base64 diretamente no navegador.**

[![Deploy static content to Pages](https://github.com/claudemirtech/base64/actions/workflows/static.yml/badge.svg)](https://github.com/claudemirtech/base64/actions/workflows/static.yml)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Client-Side Only](https://img.shields.io/badge/Processamento-100%25%20Client--Side-brightgreen?style=flat-square)

[**Acessar a Ferramenta Online**](https://atomicweb.com.br/base64) • [**Reportar Problema**](https://github.com/claudemirtech/base64/issues)

</div>

---

## 📌 Sobre o Projeto

O **AtomicWeb - Base64** é uma ferramenta web rápida, leve e focada na privacidade desenvolvida para decodificar sequências de texto em formato **Base64** e recuperar os arquivos ou dados originais.

A aplicação conta com um sistema de identificação automática do tipo de arquivo baseado nos *magic bytes* (cabeçalhos) dos dados decodificados, permitindo identificar se o conteúdo colado se trata de um documento **PDF**, um arquivo compactado **ZIP**, um documento estruturado **XML** ou texto puro. Quando um arquivo compatível é reconhecido, botões contextuais são gerados para download imediato ou pré-visualização.

> 🔒 **Privacidade em primeiro lugar:** Todo o processamento é executado localmente (100% *client-side*) no seu próprio navegador. Nenhum dado colado é enviado para servidores externos ou armazenado em banco de dados.

---

## ✨ Funcionalidades

- **⚡ Decodificação Instantânea:** Converte payloads em Base64 para texto ou formato binário de forma simples e rápida.
- **🔍 Detecção Automática de Tipo de Arquivo:**
  - **PDF (`%PDF`)**: Disponibiliza botão para download com extensão `.pdf` e pré-visualização integrada diretamente no navegador.
  - **ZIP (`PK`)**: Permite baixar o arquivo compactado `.zip` com um clique.
  - **XML (`<?xml`, `<![C`, etc.)**: Reconhece documentos XML e disponibiliza o download com extensão `.xml`.
  - **Texto / Outros**: Exibe o conteúdo decodificado na caixa de saída de texto.
- **📥 Download Automático com Timestamp:** Salva o arquivo gerado com a extensão apropriada e nome formatado com data e hora local (ex.: `25-10-2026-16-55-00.pdf`).
- **👁️ Pré-visualização Integrada:** Suporte para abrir e visualizar documentos PDF embutidos diretamente no navegador.
- **🎨 Interface Moderna e Responsiva:** Desenvolvida com **Tailwind CSS**, limpa e adaptada tanto para dispositivos móveis quanto desktop.
- **⚠️ Alertas e Validações:** Exibição amigável de notificações em caso de campo vazio ou formato Base64 corrompido/inválido.

---

## 🚀 Como Usar

1. Acesse a aplicação em **[atomicweb.com.br/base64](https://atomicweb.com.br/base64)**.
2. Cole a string em Base64 na caixa de texto superior.
3. Clique no botão **CONVERTER**.
4. O conteúdo decodificado será apresentado na caixa inferior:
   - Se for um arquivo reconhecido (**PDF**, **ZIP** ou **XML**), serão exibidos botões para **BAIXAR [TIPO]** e, no caso de PDF, **VISUALIZAR PDF**.
5. Para reiniciar a tela e limpar as caixas de texto e opções, clique em **LIMPAR**.

---

## 🛠️ Tecnologias Utilizadas

- **[HTML5](https://developer.mozilla.org/pt-BR/docs/Web/HTML)** — Estrutura semântica e acessibilidade.
- **[JavaScript (Vanilla / ES6)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)** — Funções nativas de decodificação (`atob`), detecção de cabeçalhos e manipulação do DOM.
- **[Tailwind CSS](https://tailwindcss.com/)** — Framework utilitário de CSS (via CDN) para estilização e design responsivo.
- **[GitHub Actions](https://github.com/features/actions)** — Pipeline de CI/CD para deploy contínuo no GitHub Pages.

---

## 💻 Executando Localmente

Por se tratar de uma aplicação estática e autocontida, você não precisa instalar bibliotecas externas, `npm` ou compiladores.

### 1. Clonar o repositório:
```bash
git clone https://github.com/claudemirtech/base64.git
cd base64
```

### 2. Abrir o projeto:

Basta abrir o arquivo `index.html` diretamente em seu navegador:
```bash
# Linux
xdg-open index.html

# macOS
open index.html

# Windows
start index.html
```

Ou, se preferir iniciar um servidor HTTP local simples:
```bash
# Com Python 3
python3 -m http.server 8080

# Ou com Node (npx)
npx serve .
```
E acesse `http://localhost:8080` no navegador.

---

## 🚢 Deploy e Publicação

O projeto possui integração contínua configurada através do GitHub Actions no arquivo [`.github/workflows/static.yml`](.github/workflows/static.yml).

Qualquer *push* na branch `main` dispara automaticamente o build e deploy do conteúdo estático para o **GitHub Pages**.

---

## 👨‍💻 Autor

Desenvolvido por **[Claudemir](https://github.com/claudemirtech)**.

Parte do conjunto de utilitários de **[AtomicWeb](https://atomicweb.com.br/)**.
