# Como testar e validar a solução

1. **Testar o monitoramento e o reinício automático do Nginx**

   - Pare o Nginx:
     ```bash
     systemctl stop nginx
     ```

   - Ou "mate" o processo:
     ```bash
     pkill -f nginx
     ```

   - Depois, verifique se recebeu a notificação no Telegram:

     <img width="378" height="78" alt="Image" src="https://github.com/user-attachments/assets/74f2f695-1628-4847-92e5-b589a4872d54" />)


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

     <img width="462" height="62" alt="Image" src="https://github.com/user-attachments/assets/75c32ac7-c32d-45cf-a2d6-16a06b11d318" />

   - Se precisar, corrija o fuso horário do log:  
     ```bash
     timedatectl set-timezone America/Sao_Paulo
     ```

