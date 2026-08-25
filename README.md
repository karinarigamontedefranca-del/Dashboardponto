# Pulso — Dashboard de Ponto

Site 100% estático (um único `index.html`, sem backend). Puxa os dados
direto da planilha do Google Sheets no navegador de quem estiver vendo.

## Antes de publicar
1. Na planilha, vá em **Compartilhar → Acesso geral → "Qualquer pessoa com o link" → Leitor**.
2. (Opcional, para setores) crie uma aba chamada **Setores** na mesma planilha,
   com colunas **Nome** e **Setor**. O dashboard lê essa aba ao vivo.

## Publicar no Vercel (sem precisar saber programar)

### Opção A — pela linha de comando (mais rápido)
1. Instale o Node.js, se ainda não tiver: https://nodejs.org
2. Abra o terminal nesta pasta e rode:
   ```
   npx vercel
   ```
3. Faça login quando pedir (abre o navegador) e aperte Enter nas perguntas
   (pode aceitar todos os padrões).
4. Ao final ele te dá uma URL tipo `https://seu-projeto.vercel.app` — é essa
   que você compartilha com a empresa.
5. Para atualizar depois de qualquer mudança no arquivo: rode `npx vercel --prod`
   de novo na mesma pasta.

### Opção B — pelo site do Vercel, via GitHub
1. Suba esta pasta para um repositório no GitHub.
2. Entre em https://vercel.com → **Add New → Project** → importe o repositório.
3. Deixe tudo padrão (é site estático, não precisa configurar build) → **Deploy**.
4. Pronto, o Vercel te dá a URL pública.

Qualquer atualização que você fizer na planilha (ponto ou aba de Setores)
aparece sozinha no dashboard para quem estiver com a página aberta —
não precisa reimplantar nada no Vercel para isso.
