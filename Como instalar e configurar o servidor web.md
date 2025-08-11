# Como instalar e configurar o servidor web

1. **Instale o Nginx**  
   ```bash
   sudo apt install nginx -y
   ```

2. **Crie uma página HTML inicial**
   
   Abra o arquivo no nano:
   ```bash
   sudo nano /var/www/html/index.html
   ```
   
   Digite o conteúdo html.
   
   ```bash
   Conteúdo em produção
   ```
   
   Salve com Ctrl+O, enter, Ctrl+X.
   

4. **Verifique se o Nginx está ativo**  
   ```bash
   systemctl status nginx
   ```
