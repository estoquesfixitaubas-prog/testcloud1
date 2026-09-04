# O que mudou

## 1) Correção importante (troca de nomes)
Como você renomeou os arquivos (`landing.html` → `index.html`, e o catálogo antigo `index.html` → `catalogo.html`), o `admin.html` e o `sw.js` ainda estavam configurados pros nomes antigos. Corrigi:

- O painel (`admin.html`) agora lê e salva o catálogo em `catalogo.html` (antes tentava mexer no `index.html`, que hoje é a landing).
- O `sw.js` agora guarda os dois arquivos (`index.html` e `catalogo.html`) no cache offline, e a página de fallback (quando a internet falha) passou a ser o `catalogo.html` — antes, por engano, sempre caía na landing.

## 2) Nova aba "🖥 LANDING DO SITE" no painel
Agora dá pra customizar a landing (`index.html`) direto no `admin.html`, sem mexer em código:

- **Logo**: enviar uma imagem substitui o texto "S-FIX" no cabeçalho e no rodapé (com botão pra voltar ao texto).
- **Imagem de fundo do topo (hero)**: opcional — se não enviar nada, continua o degradê de cores atual. Se enviar uma foto, o painel já aplica uma camada escura por cima automaticamente, pra manter o texto legível.
- **Foto na seção "Sobre"**: opcional, aparece acima da lista de destaques.
- **Fontes**: 4 combinações prontas (Padrão, Moderna, Clássica, Industrial) ou uma personalizada (você digita o nome da fonte e, se for do Google Fonts, o link).
- **Tamanhos de texto**: título principal, títulos de seção e texto normal, em pixels.
- **Cores**: azul, azul escuro, vermelho, teal e cor de fundo.

## Como usar
1. Abra o `admin.html` normalmente (modo automático — Chrome/Edge, selecionando a pasta — ou modo manual).
2. No modo automático, se o `index.html` estiver na mesma pasta, ele já é carregado sozinho. No modo manual, selecione-o no campo opcional "2) index.html (landing)".
3. Clique na aba **🖥 LANDING DO SITE**, ajuste o que quiser, e clique em **💾 Salvar alterações no catálogo** — ele agora salva/baixa os três arquivos junto (`catalogo.html`, `index.html` e `sw.js`).
4. Se estiver usando publicação automática via GitHub, ela também publica os três.

## O que **não** ficou editável (por enquanto)
Pra manter o escopo gerenciável, não mexi nos textos da landing (títulos, parágrafos, itens da lista de diferenciais, WhatsApp/Instagram/e-mail do rodapé) nem estruturei uma galeria de imagens além da foto única da seção "Sobre". Isso continua editável direto no código do `index.html`, como já era. Se quiser, posso incluir esses campos numa próxima rodada.
