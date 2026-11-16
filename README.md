# DK Fashion — Portfólio de soluções

Site estático que apresenta o projeto **DK Fashion** (TPPE 2026.1 e GCES 2026.2, UnB)
como vitrine para os módulos que ele oferece: loja online, pagamento e entrega,
PDV, gestão administrativa, clientes e marketing, equipe e metas.

O site é feito só com HTML, CSS e JavaScript, sem etapa de build, e pode ser
publicado direto no GitHub Pages.

## Estrutura

```text
.
├── index.html        # Início: o caso, o conceito de vitrine, módulos e números
├── solucoes.html     # Os seis módulos documentados (o que entregam, US, API)
├── engenharia.html   # Arquitetura, stack, dados, qualidade, segurança, CI/CD
├── processo.html     # Linha do tempo, clans, práticas e equipe
├── assets/
│   ├── css/style.css # Identidade visual (creme, rosa, Playfair Display + Inter)
│   ├── js/main.js    # Menu mobile, animações de entrada, sumário ativo
│   └── img/          # Imagens do frontend, modelo de dados e prints da loja
└── .nojekyll         # Faz o GitHub Pages servir os arquivos como estão
```

## Rodar localmente

```bash
python -m http.server 8000
```

Depois abra `http://localhost:8000`.

## Publicar no GitHub Pages

1. Envie este repositório para o GitHub.
2. Em **Settings → Pages**, escolha **Deploy from a branch**, branch `main` e pasta `/ (root)`.
3. O site fica em `https://<usuario-ou-org>.github.io/<repositorio>/`.

Todos os links são relativos, então o site funciona em qualquer subcaminho.

## Fontes dos dados

- Repositórios: [Frontend](https://github.com/TPPE-2026-1-Marketplace/MarketPlace-Frontend),
  [Backend](https://github.com/TPPE-2026-1-Marketplace/MarketPlace-Backend) e
  [Documentação](https://github.com/TPPE-2026-1-Marketplace/documentacao).
- Métricas de qualidade: exportações do SonarCloud em `documentacao/qa-analytics`
  (análise da `main` de 27/10/2026) e `MarketPlace-Backend/docs/cobertura-testes.md`.
- Identidade visual: apresentação "DK Fashion para Lojistas" e folder comercial (Canva).

Para atualizar os números, edite os atributos `data-count` em `index.html` e as
barras (`data-value`) em `engenharia.html`.
