# Como criar o bot do Telegram

4. **Crie um bot no Telegram**  
   - Procure o **@BotFather** na lupa do Telegram
   - 
   <img width="302" height="68" alt="Image" src="https://github.com/user-attachments/assets/e345a2ea-ca59-43bf-b1d5-08f7a2847423" />
   
   - Envie `/newbot` e siga os passos apontados pelo bot
   - Copie o token que será dado no final para usar no script
     
     <img width="413" height="67" alt="Image" src="https://github.com/user-attachments/assets/4c24abc3-1488-4973-815c-72e9d29dc062" />
     
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
