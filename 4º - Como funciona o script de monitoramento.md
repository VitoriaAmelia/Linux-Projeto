# Como funciona o script de monitoramento

1. **Crie o script**

   Crie um script para fazer o monitoramento com o editor nano no caminho /usr/local/NOME_DO_SEU_SCRIPT.sh  
 
   ```bash
   sudo nano /usr/local/bin/NOME_DO_SEU_SCRIPT.sh
   ```
   Conteúdo:  
   ```bash
   # Indique que o script será em bash
   #!/bin/bash

   # Declare as variáveis para facilitar
   
   # O token que você conseguiu do seu chat no Telegram
   TOKEN="SEU_TOKEN_AQUI"

   # O id do seu chat 
   ID="SEU_CHAT_ID_AQUI"
   
   # Endereço do se
   URL="http://localhost"
   
   # Caminho do arquivo do log que será salvo
   ARQUIVO_LOG="/var/log/NOME_DO_SEU_LOG.log"

   # Use o curl para obter o código http
   # Use -s para deixar no "modo silencioso" e não receber mensagens sobre a conexão
   # Use -o para descartar o conteúdo da página, que viria como resposta, para /dev/null
   # Ao final, a linha de código escreve o código http encontrado na URL e armazena na variável STATUS
   STATUS=$(curl -s -o /dev/null -w "%{http_code}" $URL)

   # Ecreve o código http obtido, junto com a data atual, e manda para o arquivo log
   echo "$(date): HTTP $STATUS" >> $ARQUIVO_LOG

   # se o status for diferente de 200, solicita para o telegram via POST para que ele possa mandar a mensagem indicada para o caminho fornecido
   # Depois, o nginx é reiniciado
   if [ "$STATUS" != "200" ]; then
       curl -s --request POST "https://api.telegram.org/bot$TOKEN/sendMessage" -d chat_id=$ID -d text="Alerta, site indisponível! Status: $STATUS"
       systemctl restart nginx
   fi

   ```
   
2. **Dê permissãp para executar**  
   ```bash
   sudo chmod +x /usr/local/bin/NOME_DO_SEU_SCRIPT.sh
   ```

3. **Agende a execução automática do script**  
   ```bash
   sudo crontab -e
   ```
   Adicione a linha (os "*" indicam que executa a cada minuto) : 
   ```
   * * * * * /usr/local/bin/NOME_DO_SEU_SCRIPT.SH
   ```
   
4. **Verfique**
    ```
   crontab -l
   ```

