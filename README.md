# 🌾 Cana Gestão - Sistema Agrícola

Sistema completo de gestão para produção de cana-de-açúcar, combustível, folha de pagamento e financeiro.

## ⚡ Stack

- **Frontend**: Next.js 14 + React 18 + TailwindCSS
- **Backend**: Next.js API Routes
- **Banco**: Supabase (PostgreSQL)
- **ORM**: Prisma
- **Autenticação**: Supabase Auth
- **Deploy**: Vercel

## 🚀 Quick Start

### 1. Pré-requisitos

```bash
Node.js 18+
Git
Conta Supabase (gratuita em https://supabase.com)
```

### 2. Instalação

```bash
# Clone
git clone https://github.com/jcezarvaz/canagestao.git
cd canagestao

# Instale dependências
npm install

# Configure variáveis de ambiente
cp .env.local.example .env.local
# Edite .env.local com suas credenciais Supabase

# Rode as migrações
npm run db:push

# (Opcional) Importe dados do seu JSON
npm run import:json

# Inicie o servidor
npm run dev
```

### 3. Acesse

```
Frontend: http://localhost:3000
Studio Prisma: npm run db:studio
```

## 📊 Módulos

- ✅ **Cargas** - Colheita e transbordo
- ✅ **Diesel** - Combustível
- ✅ **Folha** - Pagamentos
- ✅ **Tesouraria** - Financeiro
- ✅ **Escala** - Turnos
- ✅ **Dashboard** - Analytics

## 📁 Estrutura

```
canagestao/
├── app/
│   ├── api/                    # Endpoints
│   │   ├── cargas/
│   │   ├── diesel/
│   │   ├── folha/
│   │   ├── tesouraria/
│   │   ├── escala/
│   │   └── auth/
│   ├── dashboard/              # Dashboard principal
│   └── layout.tsx
├── components/                 # Componentes React
├── lib/                        # Utilitários
├── prisma/
│   └── schema.prisma          # Schema do banco
├── scripts/
│   ├── importar-json.js       # Importa dados
│   └── seed.js                # Dados de exemplo
└── public/                     # Assets
```

## 🗄️ Banco de Dados

Tabelas:
- `users` - Usuários
- `cargas` - Registros de colheita
- `diesel` - Movimentação de combustível
- `folha_pagamento` - Salários
- `tesouraria` - Contas
- `escala_trabalho` - Turnos
- `funcionarios` - Plantel
- `ciclos` - Períodos de faturamento

## 🔐 Autenticação

Usando Supabase Auth:
- Email/Senha
- Recuperação de senha
- Roles (Admin, Gerente, Operador)

## 📱 Responsivo

✅ Desktop
✅ Tablet
✅ Mobile

## 🚢 Deploy

### Vercel (Recomendado - Grátis)

```bash
npm install -g vercel
vercel
```

Ou conecte seu GitHub na [Vercel Dashboard](https://vercel.com).

## 📖 Documentação

Veja [SETUP.md](./docs/SETUP.md) para configuração detalhada.

## 📝 Licença

MIT
