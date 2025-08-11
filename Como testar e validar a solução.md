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

   ![Image](https://github.com/user-attachments/assets/7811b6a0-ef6c-4e3e-8bcf-1bf4b1f066d4)

   - Veja o log:
     ```bash
     cat /var/log/monitor_site.log
     ```
     
    <img width="372" height="63" alt="Image" src="https://github.com/user-attachments/assets/217b99aa-de99-4df8-92ab-ee58ebd3645a" />
    
   - Cheque o status:  
     ```bash
     systemctl status nginx
     ```
     
  


  
   
