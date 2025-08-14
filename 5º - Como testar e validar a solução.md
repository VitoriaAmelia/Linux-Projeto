# Como testar e validar a solução

1. **Testar o monitoramento e o reinício automático do Nginx**  
   - Pare o Nginx:  
     ```bash
     sudo systemctl stop nginx
     ```
     E/ou
     
   - "Mate" o processo:  
     ```bash
     sudo pkill -f nginx
     ```
     Depois:
     
   - Verifique se recebeu a notificação no Telegram:
     
   <img width="582" height="90" alt="Image" src="https://github.com/user-attachments/assets/4fa32979-b686-4adf-a815-3743eeb4796d" />

   - Veja o log:
   HTTP: 200 significa que a requisição ao servidor foi OK
     ```bash
     cat /var/log/nome_do_seu_log.log
     ```
     
   <img width="462" height="62" alt="Image" src="https://github.com/user-attachments/assets/75c32ac7-c32d-45cf-a2d6-16a06b11d318" />


   - Cheque o status:
   Inactive = inativo e active = ativo
     ```bash
     systemctl status nginx
     ```


   <img width="625" height="18" alt="Image" src="https://github.com/user-attachments/assets/43533510-d8cb-4e12-97dc-c7dd04288049" />
     
  


  
   
