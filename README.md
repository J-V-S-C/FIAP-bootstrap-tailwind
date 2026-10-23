# Vitrine de equipamentos para aventura: Bootstrap e Tailwind CSS

## Objetivo

Criar duas versões de uma mesma página de comércio eletrônico para comparar, na prática, o uso de Bootstrap e Tailwind CSS. As páginas apresentam uma seção de destaque, uma apresentação da coleção e três categorias de produtos: mochilas, calçados e jaquetas.

## Como as versões foram construídas

### Bootstrap

A versão em [`bootstrap/index.html`](bootstrap/index.html) usa Bootstrap 5.3.8 instalado pelo pnpm. O layout é organizado com `container`, `row`, `col-lg-6` e `row-cols-md-3`. Componentes e utilitários como `card`, `btn`, `ratio`, `py-5` e `text-warning` cuidam da apresentação. Os botões “Ver detalhes” abrem popovers nativos do HTML, sem JavaScript adicional.

### Tailwind CSS

A versão em [`tailwind/index.html`](tailwind/index.html) usa Tailwind CSS 4.3.3 com Vite. O arquivo [`tailwind/src/style.css`](tailwind/src/style.css) importa o Tailwind, e as classes utilitárias são aplicadas diretamente no HTML. Classes como `lg:grid-cols-2`, `md:grid-cols-3`, `bg-slate-950` e `rounded-2xl` definem layout responsivo, cores e acabamento. Os detalhes dos produtos também usam popovers nativos do HTML.

As duas páginas usam imagens externas (Pexels e, no fundo da versão Tailwind, uma imagem do Bing); por isso, é preciso ter acesso à internet para visualizá-las. O projeto é uma vitrine demonstrativa: não há carrinho, pagamentos ou servidor de dados.

## Requisitos

- Node.js e pnpm para instalar as dependências das duas versões.
- Python 3 apenas se você optar pelo servidor local sugerido para o Bootstrap.

## Como executar

Abra dois terminais a partir da raiz deste repositório.

### Bootstrap

```bash
cd bootstrap
pnpm install
python3 -m http.server 8000
```

Acesse <http://localhost:8000>. O servidor deve ser iniciado dentro da pasta `bootstrap`, pois o HTML carrega o CSS de `node_modules/bootstrap` por um caminho relativo.

### Tailwind CSS

```bash
cd tailwind
pnpm install
pnpm dev
```

Abra o endereço indicado pelo Vite no terminal, normalmente <http://localhost:5173>. Para gerar a versão de produção, execute `pnpm build` na pasta `tailwind`.

## Análise crítica

A comparação das duas tecnologias, com exemplos destas páginas, está no documento [Análise crítica — Bootstrap e Tailwind.docx](Análise%20crítica%20%E2%80%94%20Bootstrap%20e%20Tailwind.docx). O texto aborda compreensão das classes, organização, personalização, dificuldades, vantagens, limitações e a preferência fundamentada para este projeto.
