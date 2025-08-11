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
     
   - Verifique se recebeu a notificação no Telegram
     
   <img width="582" height="90" alt="Image" src="https://github.com/user-attachments/assets/4fa32979-b686-4adf-a815-3743eeb4796d" />

   - Veja o log:
     ```bash
     cat /var/log/monitor_site.log
     ```
     
   <img width="372" height="63" alt="Image" src="https://github.com/user-attachments/assets/26c30c83-9cbb-4161-974c-15f6ded656ef" />
    
   - Cheque o status:  
     ```bash
     systemctl status nginx
     ```
     
  


  
   
