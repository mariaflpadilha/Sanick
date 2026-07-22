# Site Sanick — Equipamentos de Precisão

Site institucional da Sanick Equipamentos de Precisão (Chapecó/SC).
HTML/CSS/JS estático, sem dependências de build.

## Estrutura

```
.
├── index.html            # Home
├── institucional.html    # Página institucional (história, fundadores, valores)
├── intelicount.html      # Página do produto Sanick Intelicount
├── 404.html              # Página de erro
├── netlify.toml          # Configuração de deploy (Netlify)
├── robots.txt
└── assets/               # Imagens, vídeo e documentos técnicos (PDF)
```

## Desenvolvimento local

Não há processo de build. Para visualizar localmente:

```bash
python3 -m http.server 8000
```

Depois acesse `http://localhost:8000`.

> Abrir os arquivos com duplo clique (`file://`) também funciona, mas o vídeo
> de fundo e os PDFs podem não carregar por restrição do navegador.

## Deploy (Netlify)

1. Conecte este repositório no Netlify.
2. **Build command:** deixe em branco (site estático).
3. **Publish directory:** `.` (raiz do repositório).

O `netlify.toml` já define headers de cache, segurança e os redirects de
URL amigável (`/intelicount` → `/intelicount.html`).

## Identidade visual

Definida no brandbook da marca. Referência rápida:

| Token | Valor | Uso |
|---|---|---|
| `--terracotta` | `#AC2715` | Cor primária, CTAs |
| `--terracotta-dark` | `#8A1F11` | Hover, texto sobre branco |
| `--green-darker` | `#1E3A2E` | Fundos escuros, títulos |
| `--sage` | `#7F998F` | Textos de apoio |
| `--green-accent-text` | `#8FCDA8` | Destaques sobre fundo escuro |
| `--ink` | `#242422` | Texto principal |
| `--gray-text` | `#5B6560` | Texto secundário |

**Tipografia:** Inter (títulos) · IBM Plex Sans (corpo) · JetBrains Mono (dados e specs).

## Pendências

- [ ] Substituir os depoimentos ilustrativos da página do Intelicount por depoimentos reais de clientes.
- [ ] Definir se o mural de logos de clientes entra também na página institucional.
- [ ] Configurar captura de leads (Netlify Forms) no formulário de contato da home.
