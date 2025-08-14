# Como configurar o ambiente

1. **Instale a VirtualBox**
     
   - Link para download: [https://www.virtualbox.org/](https://www.virtualbox.org/)

3. **Baixe o Ubuntu**
   
   - Acesse o link:[https://ubuntu.com/download/server](https://ubuntu.com/download/server)
   - Faça o download da imagem ISO do Ubuntu Server 24.04.3 LTS

2. **Crie uma VM**
   
   - 1,8 GB RAM, 1 CPU e 25 GB no tamanho do disco são suficientes  
   - Em configurações da VM > Rede > Adaptador 1, use a Placa em modo Bridge (para que a VM compartilhe a internet do computador hospedeiro)
   - Não se esqueça de adicionar a imagem ISO, em configurações da VM > Armazenamento > Controladora IDE

4. **Primeiros passos**
   
   - Faça login com usuário e senha definidos na instalação
   - Digite:  
   ```bash
   sudo su root
   ```
   - Digite a senha do usuário
   - Volte para o diretório raiz:
   ```bash
   cd /
   ```  
   
5. **Atualize**
    
   Após a instalação, atualize a lista de pacotes disponíveis e instale todas as atualizações disponíveis:  
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```
