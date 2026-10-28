# Site — Michelle Martins, Advogados Associados

Pasta pronta para subir. Tudo o que o site precisa está aqui dentro e nada mais:

| Arquivo | Para quê |
|---|---|
| `index.html` | O site inteiro (HTML, CSS e JavaScript no mesmo arquivo) |
| `img/` | Fundos e fotos otimizados em WebP (~0,8 MB no total, inclui as fotos da Michelle) |
| `.nojekyll` | Diz ao GitHub Pages para publicar os arquivos como estão |
| `.gitignore` | Evita subir lixo do Mac (`.DS_Store`) |

> **Estado atual: rascunho para revisão.** O `index.html` ainda tem a faixa "Rascunho", as marcações amarelas (itens que dependem da cliente) e a meta `noindex` (o Google não indexa). Veja "Antes de divulgar" abaixo.

## Subir no GitHub

**Jeito 1 — pelo navegador (sem terminal)**
1. Em github.com/new crie um repositório (sugestão de nome: `michelle-martins-site`). Sem README, sem `.gitignore`, sem licença.
2. Na página do repositório vazio, clique em **uploading an existing file**.
3. Arraste **o conteúdo** desta pasta (o `index.html`, a pasta `img` e os arquivos ocultos `.nojekyll` e `.gitignore`; no Finder, `Cmd + Shift + .` mostra os ocultos) e clique em **Commit changes**.

**Jeito 2 — pelo terminal**, dentro desta pasta:
```bash
git init -b main
git add .
git commit -m "Site Michelle Martins (rascunho)"
git remote add origin https://github.com/SEU-USUARIO/michelle-martins-site.git
git push -u origin main
```

## Colocar no ar (GitHub Pages)
1. No repositório: **Settings → Pages**.
2. Em **Build and deployment**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`, e salve.
3. Em 1–2 minutos o site abre em `https://SEU-USUARIO.github.io/michelle-martins-site/`.

**Atenção:** no plano gratuito do GitHub, o Pages só funciona com repositório **público**. Se quiser o código privado, use o **Netlify** (arraste esta pasta em app.netlify.com/drop) ou o Cloudflare Pages, que aceitam repositório privado de graça.

## Antes de divulgar o link
O endereço fica acessível a quem tiver o link, mesmo com `noindex`, e **as fotos da Michelle estão em `img/`**: em repositório público elas ficam abertas a qualquer pessoa. Antes de mandar pra cliente ou publicar de verdade:
- [ ] Preencher OAB, áreas de atuação, WhatsApp e demais dados que a cliente confirmar (itens em amarelo)
- [ ] Trocar o logo provisório (texto) pelo arquivo oficial
- [ ] Revisar os textos contra as regras de publicidade da OAB
- [ ] No `index.html`: remover a faixa `<div class="draft"…>` (e o JS dela), as marcações `.tbd` e a linha `<meta name="robots" content="noindex,nofollow">`
- [ ] Testar no celular

## Domínio próprio (quando houver)
Crie um arquivo chamado `CNAME` nesta pasta, com uma única linha: o domínio (ex.: `www.michellemartins.adv.br`), e configure o DNS conforme a documentação do GitHub Pages.

---
*Esta pasta é uma cópia de `../site/`. Quando o site for alterado em `../site/`, copie de novo os arquivos para cá (ou peça ao Claude: "atualiza a pasta GITHUB").*
