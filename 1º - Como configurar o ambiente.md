# Como configurar o ambiente

1. **Instale a VirtualBox**  
   - Link par baixar: [https://www.virtualbox.org/](https://www.virtualbox.org/)

2. **Baixe o Ubunto**
   - Acesse o link:[ https://ubuntu.com/download/desktop](https://ubuntu.com/download/desktop)
   - Escolha o Ubuntu Server (Ubuntu 22.04 LTS)

2. **Crie uma VM**  
   - 1,8 GB RAM e 1 CPU são suficientes  
   - Sobre a rede, use a Placa em modo Bridge (para usar a internet do computador que hospeda a VM)

3. **Atualize**  
   Após a instalação, atualize a lista de pacotes disponíveis e instale todas as atualizações disponíveis:  
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```
