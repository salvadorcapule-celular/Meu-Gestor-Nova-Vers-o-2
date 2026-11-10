# Meu Gestor — publicação no GitHub Pages

Este pacote contém a aplicação Meu Gestor V8.2.3, preparada como PWA (aplicação web instalável), com suporte a cache offline da estrutura principal.

## Conteúdo

- `index.html` — aplicação principal (inclui o botão Menu).
- `manifest.webmanifest` — nome, ícones e configuração de instalação.
- `sw.js` — service worker para cache e acesso offline à estrutura da aplicação.
- `favicon.png` e `assets/icons/` — ícones para navegador e instalação.
- `.nojekyll` — evita processamento Jekyll do GitHub Pages.

## Publicar no GitHub Pages

1. Entre em https://github.com e crie um repositório novo, por exemplo `meu-gestor`.
2. Extraia este ZIP no seu computador ou telemóvel.
3. Envie **todos os ficheiros e pastas que estão dentro** de `meu-gestor-github-pages` para a raiz do repositório. O `index.html` deve ficar directamente na raiz, não dentro de uma segunda pasta.
4. No GitHub, abra **Settings → Pages**.
5. Em **Build and deployment**, escolha **Deploy from a branch**.
6. Seleccione a branch `main` e a pasta `/ (root)`; carregue em **Save**.
7. Aguarde a publicação e abra o endereço apresentado pelo GitHub Pages. Normalmente será `https://SEU utilizador.github.io/meu-gestor/` (sem espaços; substitua pelo seu utilizador e repositório reais).

## Instalar no telemóvel Android

1. Abra o endereço HTTPS publicado no Chrome.
2. Abra o menu do Chrome (⋮).
3. Escolha **Instalar aplicação** ou **Adicionar ao ecrã inicial**.

## Actualizar a aplicação

Substitua os ficheiros no repositório pelos novos e faça commit. Se o navegador continuar a mostrar uma versão antiga, feche e volte a abrir a aplicação ou limpe os dados/cache do site. Ao alterar os ficheiros da aplicação, actualize também o identificador `CACHE_NAME` em `sw.js` (por exemplo, termine em `cache-2`) para forçar um novo cache.

## Nota importante sobre os dados

Os dados do Meu Gestor são guardados localmente no navegador/dispositivo. O GitHub Pages publica os ficheiros da aplicação, mas **não sincroniza automaticamente os dados entre telemóveis ou computadores**. Faça regularmente cópias de segurança dentro da aplicação e guarde os ficheiros exportados num local seguro. Limpar os dados do navegador pode apagar os registos locais.

O GitHub Pages serve a aplicação por HTTPS, requisito para o service worker e para a instalação PWA. Não é necessário criar servidor ou base de dados para esta versão local.


## Actualização visual e navegação

- Ícone da aplicação renovado para Android/PWA (192 px, 512 px, máscara e Apple Touch Icon).
- O botão **Abrir menu** da página inicial abre agora uma página própria **Menu principal**.
- A página Menu tem botão **Voltar à página inicial** e atalhos para todas as áreas.


## PWA / Instalação

O pacote inclui `manifest.webmanifest` e `sw.js`. Envie todos os ficheiros e pastas para a raiz do repositório GitHub Pages, mantendo `assets/icons/`. Aguarde a publicação e abra o endereço HTTPS no Chrome Android.
