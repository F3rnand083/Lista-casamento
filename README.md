
# Site de Lista de Casamento — Pacote Final

Este pacote inclui:
- **Nomes editáveis** no próprio site (com `localStorage` e suporte a parâmetros de URL)
- **Botões fixos** (A, B, Ambos) para enviar mensagem via WhatsApp
- **Envio para os dois** em sequência (com fallback "Abrir 2º envio" se o navegador bloquear pop-up)
- **Imagens por link (HTTPS)** para capa, cotas e galeria

## Como usar
1. Publique os arquivos em um repositório no GitHub e habilite **GitHub Pages** ou suba em qualquer hospedagem estática.
2. Edite no arquivo **`index.html`**:
   - **Números de WhatsApp** (DDI+DDD+número):
     ```js
     const NUMERO_A = "5511999999999"; // Nome 1
     const NUMERO_B = "5511988888888"; // Nome 2
     ```
   - **Imagens por link** (substitua as URLs `https://images.unsplash.com/...` pelas suas)
   - **RSVP**: troque `SEU_FORM_ID` do Google Forms
3. Nomes dos noivos:
   - Use a seção **“Editar nomes dos noivos”** para alterar e **Salvar nomes** (persistem no navegador)
   - Ou preencha via URL: `?noivo=Luiz&noiva=Ana` (ou `?nome1=...&nome2=...`)

## Observações
- **WhatsApp** não permite um único link para dois números ao mesmo tempo. Por isso, o botão **Ambos** abre A e depois B em sequência. Se o 2º pop-up for bloqueado, use o botão **“Abrir 2º envio”** que aparece no dock.
- Use **HTTPS** nas imagens para evitar bloqueio de conteúdo misto.
- Recomendo imagens em proporção **3:2** para os cards (ex.: 1200×800, JPG 80%).
