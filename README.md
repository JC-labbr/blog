# 📖 Entre Páginas — Blog & Revista Literária

Blog de crítica literária independente com painel CMS integrado ao Supabase.

## 🚀 Stack

- **Frontend**: HTML5 + Tailwind CSS (CDN) + Lucide Icons
- **Backend / Banco de Dados**: [Supabase](https://supabase.com)
- **Autenticação**: Supabase Auth (e-mail + senha)
- **Hospedagem**: Qualquer serviço estático (Netlify, Vercel, GitHub Pages, etc.)

## 📁 Estrutura

```
blog/
├── index.html          # Aplicação principal (SPA)
├── README.md           # Documentação
├── netlify.toml        # Config Netlify (redirects SPA)
├── vercel.json         # Config Vercel (redirects SPA)
├── _headers            # Headers HTTP (segurança)
└── .github/
    └── workflows/
        └── deploy.yml  # CI/CD automático
```

## ⚙️ Configuração do Supabase

As credenciais já estão configuradas no `index.html`:

| Variável | Valor |
|----------|-------|
| `SUPABASE_URL` | `https://evfujanqkaoaxurknseg.supabase.co` |
| `SUPABASE_ANON_KEY` | configurada no index.html |

## 🔐 Acesso Admin

| Campo | Valor |
|-------|-------|
| URL do Painel | `/` → botão **Admin** no header |
| E-mail | `admin@entrepaginas.com.br` |
| Senha | `EntreP@ginas2026!` |

> ⚠️ **Importante**: Altere a senha após o primeiro login via painel do Supabase em **Authentication → Users**.

## 🗄️ Tabelas do Banco de Dados

| Tabela | Descrição |
|--------|-----------|
| `books` | Livros e resenhas |
| `authors` | Perfis de autores |
| `reading_lists` | Listas de leitura curadas |
| `comments` | Comentários dos leitores |
| `helpful_votes` | Votos de utilidade das resenhas |

## 🌐 Deploy Rápido

### Netlify
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start)

1. Faça fork deste repositório
2. Conecte ao Netlify → "New site from Git"
3. Build command: *(deixe vazio)*
4. Publish directory: `.` (raiz)
5. Deploy!

### Vercel
1. Importe o repositório no [vercel.com](https://vercel.com)
2. Framework Preset: **Other**
3. Output Directory: `.`
4. Deploy!

### GitHub Pages
1. Vá em **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` / pasta: `/ (root)`
4. Save!

## 🛠️ Desenvolvimento Local

```bash
# Clone o repositório
git clone https://github.com/JC-labbr/blog.git
cd blog

# Sirva localmente (qualquer servidor estático)
npx serve .
# ou
python3 -m http.server 3000
# ou
php -S localhost:3000
```

Acesse: `http://localhost:3000`

## 📝 Como Publicar uma Nova Resenha

1. Acesse o blog e clique em **Admin** no header
2. Faça login com as credenciais acima
3. Na aba **Nova Postagem**, preencha o formulário
4. A resenha completa suporta **HTML** para formatação rica
5. Marque **Destaque na Página Inicial** para fixar como featured
6. Clique em **Publicar Resenha**

## 📄 Licença

© 2026 Entre Páginas Periódico Cultural. Todos os direitos reservados.
