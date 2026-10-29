# Sport Life — catálogo estático para GitHub Pages

O site é estático: HTML, CSS e JavaScript. Um workflow do GitHub Actions gera `catalog.json` a partir das pastas e publica o site. Você não precisa instalar Python no seu computador; o script roda nos servidores do GitHub.

## Estrutura das camisetas

Coloque cada produto numa pasta dentro da categoria correspondente:

```text
camisetas/
  Masculinas/
    Camiseta Brasil/
      01-frente.jpg
      02-costas.jpg
  Femininas/
    Camiseta Brasil Feminina/
      01-frente.jpg
```

Aceita JPG, JPEG, PNG, WEBP, GIF, AVIF e BMP. Os nomes das pastas são os nomes dos produtos; números nos nomes dos arquivos definem a ordem das fotos. O catálogo é gerado automaticamente durante a publicação.

## Publicar

1. Crie um repositório no GitHub chamado `sportlife`.
2. Envie o conteúdo desta pasta para a raiz do repositório, incluindo a pasta oculta `.github`.
3. Em **Settings → Pages → Build and deployment**, selecione **GitHub Actions** como fonte.
4. Em **Settings → Actions → General**, confirme que Actions tem permissão para executar workflows e publicar Pages.
5. Em `script.js`, altere `WHATSAPP_NUMBER` para o número da loja com código do país + DDD + número, somente dígitos (ex.: `5511999999999`, substituindo pelo número real).
6. Faça commit/push. Abra **Actions** para acompanhar a publicação; depois o endereço aparece em **Settings → Pages**.

Quando adicionar/alterar imagens, envie as alterações para o repositório. O workflow gera novamente o catálogo e publica a atualização. Nenhum Python precisa ser instalado ou executado no seu computador.

## Observações

- O GitHub Pages publica imagens do próprio repositório; não descobre pastas no computador do visitante.
- Não incluí fotos de produtos porque elas não foram fornecidas nesta conversa.
- Para 10 mil produtos, imagens pesadas podem deixar o site lento e o repositório muito grande. Redimensione/comprima fotos e considere usar paginação ou carregamento progressivo.
- O botão de WhatsApp está configurado como exemplo; substitua o número antes de publicar.
