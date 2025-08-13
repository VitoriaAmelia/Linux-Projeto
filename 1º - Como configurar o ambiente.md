# Como configurar o ambiente

1. **Instale a VirtualBox**  
   - Link para download: [https://www.virtualbox.org/](https://www.virtualbox.org/)

2. **Baixe o Ubunto**
   - Acesse o link:[ https://ubuntu.com/download/desktop](https://ubuntu.com/download/desktop)
   - Escolha o Ubuntu Server (Ubuntu 22.04 LTS) e faça download

2. **Crie uma VM**  
   - 1,8 GB RAM e 1 CPU são suficientes  
   - Sobre a rede, use a Placa em modo Bridge (para usar a internet do computador que hospeda a VM)

3. **Atenção à senha!**
   - Durante a configuração da VM, é necessário informar a senha de usuário
   - Guarde essa senha, pois ela será necessária para executar alguns comandos sudo

5. **Atualize**  
   Após a instalação, atualize a lista de pacotes disponíveis e instale todas as atualizações disponíveis:  
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```
