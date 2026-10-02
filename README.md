# SRJ Business — site institucional

Site oficial da **SRJ Business** — *Construindo negócios mais preparados para o futuro*.

Grupo de soluções e resultados na jornada dos negócios: estratégia, gestão, tecnologia e presença digital para pequenos negócios, MEIs, autônomos e empresas em desenvolvimento.

## Tecnologia

Site estático, sem build e sem dependências:

- HTML5 semântico (`index.html`)
- CSS puro com variáveis (`assets/css/styles.css`)
- JavaScript puro, ~3 KB (`assets/js/main.js`): menu mobile, navbar ao rolar, seção ativa, entrada suave dos elementos, voltar ao topo e ano automático
- Fontes hospedadas no próprio site (Manrope e Cormorant Garamond, licença SIL OFL)
- Respeita `prefers-reduced-motion`

## Estrutura

```
.
├── index.html            Página principal (todas as seções)
├── 404.html              Página de erro
├── favicon.ico
├── site.webmanifest
├── robots.txt
├── sitemap.xml
├── .nojekyll             Desativa o Jekyll no GitHub Pages
└── assets/
    ├── css/styles.css
    ├── js/main.js
    ├── fonts/            Fontes .woff2
    └── img/              Logos, ícones, imagens da identidade e og-image
```

Seções da página: Início · A SRJ · Jornada · Soluções · Como funciona · Para quem · Empresas · Contato.

Para criar novas páginas no futuro (ex.: `planos.html`), reutilize o mesmo `<header>`, `<footer>` e `assets/css/styles.css`.

## Rodar localmente

```bash
python3 -m http.server 8000
# abra http://localhost:8000
```

## Publicação (GitHub Pages)

1. **Settings → Pages**
2. Source: **Deploy from a branch** · Branch: **main** · Pasta: **/ (root)**
3. Endereço atual: https://srjbusiness.github.io/srj-business/

Todos os caminhos de arquivos são relativos, então o site funciona tanto no endereço do GitHub Pages quanto em um domínio próprio.

## Contatos usados no site

| Canal | Valor |
|---|---|
| WhatsApp Business | +55 35 99145-5040 (`https://wa.me/5535991455040`) |
| E-mail | gpsrjbusiness@gmail.com |
| Instagram | https://www.instagram.com/srjbusiness_/ |
| Facebook | https://www.facebook.com/profile.php?id=61594988819561 |

Para trocar o número do WhatsApp, procure por `5535991455040` em `index.html` e substitua todas as ocorrências.

### Adicionar o LinkedIn

O LinkedIn já está preparado, mas desativado (não há link falso):

1. Em `index.html`, procure por `LINKEDIN:` (2 lugares: seção Contato e rodapé), descomente o bloco e troque `URL_DO_LINKEDIN` pelo endereço real.
2. No bloco `application/ld+json` do `<head>`, adicione a URL do LinkedIn na lista `sameAs`.

## Domínio próprio (futuro)

Quando houver um domínio oficial (ex.: registrado no Registro.br):

1. Em **Settings → Pages → Custom domain**, informe o domínio (o GitHub cria o arquivo `CNAME`).
2. No Registro.br, configure o DNS:
   - domínio raiz: registros **A** para `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `www`: registro **CNAME** para `srjbusiness.github.io`
3. Marque **Enforce HTTPS**.
4. Troque a URL `https://srjbusiness.github.io/srj-business/` pela nova em: `index.html` (canonical, Open Graph, Twitter e JSON-LD), `sitemap.xml`, `robots.txt` e `404.html`.

Observação: em um site de projeto (`/srj-business/`), o `robots.txt` não fica na raiz do domínio e é ignorado pelos buscadores; com domínio próprio ele passa a valer. O `sitemap.xml` pode ser enviado manualmente no Google Search Console.

## Conta GitHub

- Conta: https://github.com/srjbusiness
- Repositório: https://github.com/srjbusiness/srj-business
- Site: https://srjbusiness.github.io/srj-business/

A conta foi renomeada de `gpsrjbusiness-cmd` para `srjbusiness`. O GitHub redireciona o repositório antigo, mas não redireciona o endereço antigo do GitHub Pages.

O e-mail `gpsrjbusiness@gmail.com` é o endereço real de contato da empresa e não depende do nome da conta.
