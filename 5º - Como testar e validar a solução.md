# Como testar e validar a solução

1. **Testar o monitoramento e o reinício automático do Nginx**

   - Pare o Nginx:
     ```bash
     sudo systemctl stop nginx
     ```

   - Ou "mate" o processo:
     ```bash
     sudo pkill -f nginx
     ```

   - Depois, verifique se recebeu a notificação no Telegram:

     ![Notificação Telegram](https://github.com/user-attachments/assets/4fa32979-b686-4adf-a815-3743eeb4796d)


   - Cheque o status:
     - `Inactive` = inativo
     - `Active` = ativo
     ```bash
     systemctl status nginx
     ```

     ![Status Nginx](https://github.com/user-attachments/assets/43533510-d8cb-4e12-97dc-c7dd04288049)


   - Veja o log:  
     HTTP 200 significa que a requisição ao servidor foi OK
     ```bash
     cat /var/log/nome_do_seu_log.log
     ```
