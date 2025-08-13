# Como criar o bot do Telegram

4. **Crie um bot no Telegram**  
   - Procure o **@BotFather** na lupa do Telegram  
   - Envie `/newbot` e siga os passos apontados pelo bot
   - Copie o token que será dado no final para usar no script

5. **Ache o ID do seu chat**  
   - No navegador, acesse com seu token:
     
     ```
     https://api.telegram.org/botSEU_TOKEN_AQUI/getUpdates
     ```
     
   - Envie uma mensagem para o bot no Telegram para criar o id do seu chat
     
   - Recarregue a página do navegador e procure algo como:  
     ```
     "id": 123456789
     ```
     Esse será o id do seu chat
