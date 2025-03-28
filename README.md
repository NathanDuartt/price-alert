# Espião de Preço

Uma aplicação web moderna para monitorar preços de produtos online.

## Configuração do Ambiente

1. Clone o repositório
```sh
git clone <URL_DO_REPOSITORIO>
cd espiao-de-preco
```

2. Instale as dependências
```sh
npm install
```

3. Configure as variáveis de ambiente
```sh
cp .env.example .env
# Edite o arquivo .env com suas configurações
```

## Desenvolvimento

Para iniciar o servidor de desenvolvimento:
```sh
npm run dev
```

## Build e Deploy

1. Gere a build de produção:
```sh
npm run build:prod
```

2. O código otimizado estará na pasta `dist/`

### Deploy em diferentes plataformas:

#### Vercel
- Conecte seu repositório GitHub à Vercel
- A Vercel detectará automaticamente que é um projeto Vite
- Configure as variáveis de ambiente no painel da Vercel

#### Netlify
- Conecte seu repositório GitHub ao Netlify
- Comando de build: `npm run build:prod`
- Diretório de publicação: `dist`
- Configure as variáveis de ambiente no painel do Netlify

#### GitHub Pages
1. No arquivo `vite.config.ts`, adicione sua base URL:
```ts
export default defineConfig({
  base: '/seu-repositorio/',
  // ... outras configurações
})
```

2. Deploy usando GitHub Actions (já configurado)
- Faça push para a branch main
- O GitHub Actions fará o build e deploy automaticamente

## Estrutura do Projeto

```
espiao-de-preco/
├── src/
│   ├── components/     # Componentes React reutilizáveis
│   ├── pages/         # Páginas da aplicação
│   ├── hooks/         # Custom hooks
│   └── lib/           # Utilitários e configurações
├── public/            # Arquivos estáticos
└── dist/             # Build de produção
