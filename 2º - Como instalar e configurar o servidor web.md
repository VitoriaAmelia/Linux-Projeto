# Como instalar e configurar o servidor web

1. **Instale o Nginx**
   
   ```bash
   sudo apt install nginx -y
   ```
   
3. **Verifique se o Nginx está ativo**
   
   ```bash
   systemctl status nginx
   ```
   
3. **Antes de criar sua página, considere como enviar imagens para a VM**
   
   No computador local, nesse caso o Windows, digite o modelo no cmd:
   
    ```bash
   scp "C:\caminho\sua_imagem.extensao" usuario@ip_servidor:/home/usuario/
   ```
      
   C:\caminho\sua_imagem.extensao --> caminho da imagem no seu computador
   
   usuario --> seu usuário na VM
        
   ip_servidor --> ip da sua máquina

   Será necessário, depois desse processo, digite a senha do usuário da VM

   Na Máquina Virtual, digite:

    ```bash
   sudo mv /home/usuario/imagem.extensao /var/www/html/
   ```
   Isso moverá seu arquivo para o mesmo diretório onde estará a página HTML.
   Será necessário digitar a senha do usário novamente   
5. **Crie uma página HTML inicial**
   
   Abra o arquivo "index.html" no editor nano, precisa ser nesse caminho:
   
   ```bash
   sudo nano /var/www/html/index.html
   ```
   
   Digite o conteúdo html:
   
   ```bash
   Conteúdo em produção
   ```
   
   Salve com Ctrl+O, enter, Ctrl+X.

6. **Veja o ip da sua máquina**
   
   ```bash
   ip -4 a
   ```
   
7. **Cole no navegador**
   
   ```bash
   http://IP_CONSULTADO
   ```
   

