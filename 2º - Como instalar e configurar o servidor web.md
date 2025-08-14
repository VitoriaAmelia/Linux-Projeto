# Como instalar e configurar o servidor web

1. **Instale o Nginx**
   
   ```bash
   apt install nginx -y
   ```
   
3. **Verifique se o Nginx está ativo (procure por "active:running")**
   
   ```bash
   systemctl status nginx
   ```
   
3. **Antes de criar sua página, considere como enviar imagens para a VM**
   
   No computador local, nesse caso o Windows, digite o modelo no cmd como administrador:
   
    ```bash
   scp "C:\caminho\sua_imagem.extensao" usuario@ip_servidor:/home/usuario/
   ```
      
   C:\caminho\sua_imagem.extensao --> caminho da imagem no seu computador
   
   usuario --> seu usuário na VM
        
   ip_servidor --> ip da sua máquina

   Na Máquina Virtual, digite:

    ```bash
   mv /home/usuario/imagem.extensao /var/www/html/
   ```
   Isso moverá seu arquivo para o mesmo diretório onde estará a página HTML.
    
5. **Crie uma página HTML inicial**
   
   Abra o arquivo "index.html" no editor nano, precisa ser nesse caminho:
   
   ```bash
   nano /var/www/html/index.html
   ```
   
   Digite o conteúdo html:
   
   ```bash
 	<!DOCTYPE html>
	<html lang="pt-BR">
	<head>
	<meta charset="UTF-8" />
	<title> Projeto Linux </title>
	<style>
	body{
	font-family: Arial, sans-serif;
	margin: 0;
	padding: 0;
	background-color: #121212;
	color: #e0e0e0;
	line-height: 1.8;
	font-size: 16px;	
	}
	
	header{
	background-color: #1f1f1f;
	color: white;
	font-weight: bold;
	padding: 20px;
	text-align: center;
	box-shadow: 0 2px 6px #000000cc;
	}

	header h1{
	margin: 0;
	font-weight: normal;
	}

	main{
	max-width: 900px;
	padding: 20px;
	margin: auto;
	}

	section{
	background: #1f1f1f;
	padding: 15px;
	margin-bottom: 20px;
	border-radius: 5px;
	box-shadow: 0 0 8px #000000cc;
	}
	
	section h2{
	border-bottom: 2px solid #90caf9;
	padding-bottom: 5px;
	color: #90caf9;
	}

	ul, ol{
	line-height: 1.6;
	color: #cccccc;
	font-size: 18px;
	}

	p{
	font-size: 18px;
	}
	.titulo-icon{
	width: 44px;
	height: 44px;
	border-radius: 50%;
	vertical-align: midlle;
	margin-right: 8px;
	object-fit: cover;
	}
	h2{
	display: flex;
	align-items: center;
	gap: 8px;
	}
	.gif{
	width: 170px;
	height: 100px;
	}
	
	</style>
	</head>
	
	<body>
		<header>
			<h1><strong>Projeto Linux</strong> </h1>
		</header>
	<main>
		<center><img src="linux_gif.gif" class="gif"/></center>
		
		<section>
			<h2><img src="info.png" class="titulo-icon"/> Sobre o projeto </h2>
			<p>Esse Projeto monitora automaticamente a disponibilidade de um site e envia notificações caso ele fique indisponível. Ele também mantém logs e garante que o servidor esteja sempre no ar.</p>
		</section>
		<section>
		<h2><img src="importante.png" class="titulo-icon"/> Importância do projeto</h2>
		<p>Monitorar um site é importante para garantir a disponibilidade e evitar prejuízos que podem ocorrer caso alguma falha não seja detectada de forma rápida.		
		</section>
		
		<section>
			<h2><img src="prancheta.png" class="titulo-icon"/> Requistos do projeto </h2>
			<ul>
			<li> Ubunto Server instalado </li>
			<li> Servidor Web Nginx </li>
			<li>Script de monitoramento</li>
			<li>Bot do Telegram configurado </li>
			<li>Agendamento da tarefa </li>
			</ul>
		</section>
		
		<section>
	  		<h2><img src="git.png" class="titulo-icon"/>Ordem de passos a serem seguidos no GitHub</h2>
			<ol>
			<li>Como configurar o ambiente</li>
			<li>Como instalar e configurar o servidor web</li>
			<li>Como criar o bot do Telegram</li>
			<li>Como funciona o script de monitoramento</li>
			<li>Como testar e validar a solução</li>
			</ol>
			<p>Endereço: https://github.com/VitoriaAmelia/Linux-Projeto-1.git </p>
		</section>
		
		<section>
			<h2><img src="perfil.png" class="titulo-icon"/> Desenvolvedora</h2>
			<p>Vitoria Silva desenvolveu o projeto no contexto do programa de bolsas.</p>
		</section>
	
	</body>
	</html>
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
   

