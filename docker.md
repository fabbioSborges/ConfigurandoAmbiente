# Docker


![](https://blog.geekhunter.com.br/wp-content/uploads/2019/07/business-1845350_960_720-min-768x512.jpg)


Um Container é a forma de empacotar sua aplicação e suas dependências (bibliotecas) de forma padronizada. 

As palavras chaves para o Docker são: construir, entregar e rodar em qualquer ambiente (develop, ship and run anywhere).

Os principais componentes da arquitetura envolvem:

  - Docker para Mac, Linux e Windows – versões que permitem instalar e executar containers nos sistemas operacionais de forma isolada.
  - Docker Daemon – Software que roda na máquina onde o Docker está instalado. Usuário não interage diretamente com o daemon.
  - Docker Client – CLI ou REST API que aceita comandos do usuário e repassa estes comandos ao Docker daemon.
  - Docker Image – É um template. Uma imagem contém todos os dados e metadados necessários para executar containers a partir de uma imagem.
  - Docker Container –  Detém tudo que é necessário para uma aplicação ser executada. Cada container é criado a partir de uma imagem. Cada container é uma aplicação isolada independente.
  - Docker Engine – Usado para criar imagens e containers.
  - Docker Hub – Este é um registro usado para hospedar e baixar diversas imagens. Pode ser visto como uma plataforma SAAS de compartilhamento e gerenciamento de imagens.
  - Dockerfile –  Um arquivo texto contendo uma sintax simples para criação de novas imagens.
  - Docker Compose – Usado para definir aplicações usando diversos containers.
  
 
 ## Instalação 
 
 1. Configurando repositorio
  
        $ sudo apt-get update

        $ sudo apt-get install \
            apt-transport-https \
            ca-certificates \
            curl \
            gnupg-agent \
            software-properties-common
  2. Adicionar Docker GPG key
       
          curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
  
  3. Adicionar o repositorio estavel
  
          sudo add-apt-repository \
         "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
         $(lsb_release -cs) \
         stable"
     
   4. Instalar o docker
   
          sudo apt-get update
          sudo apt-get install docker-ce docker-ce-cli containerd.io
    
   5. Verificar que a instalação foi correta
        
          sudo docker run hello-world
      
   6. Gerenciar o Docker como um usuário não root

          O daemon Docker se liga a um soquete Unix em vez de uma porta TCP. Por padrão, esse soquete Unix é propriedade do usuário roote outros usuários só podem acessá-lo usando sudo. O daemon Docker sempre é executado como o rootusuário.

          Se você não quiser iniciar o dockercomando com sudo, crie um grupo Unix chamado dockere adicione usuários a ele. Quando o daemon do Docker é iniciado, ele cria um soquete Unix acessível aos membros do dockergrupo.
      
          6.1. Criar o grupo docker
            
            sudo groupadd docker
            
          6.2 Adicionar o usuario ao grupo docker
             
             sudo usermod -aG docker $USER
          6.3 realizar o logout 
              newgrp docker 
          6.4 verificar se é possivel executar o docker sem o sudo
              do
            
      
      

  

 
