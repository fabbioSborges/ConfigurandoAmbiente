# Primeira aplicação

1. Abrir o VSCode

2. Criar uma pasta 
  PrimeiraAplicação
  
3. Criar o arquivo package json
  yarn init -y
    {
      "name": "primeiraAplicação",
      "version": "1.0.0", //versão 
      "main": "index.js",
      "license": "MIT"
    }

  package.json = guarda as dependendcias da aplicação
  
4. Instalar a dependencia Express
  microfamework do node
  yarn add express

5. criar o arquivo index.js

            const express = require('express');
            const server = express(); //chamar a função express
            server.get('/teste', (req,res) => {
              console.log("teste");
              //return res.send("Olá Turma"); // retornar texto
              return res.json({mensagem: "olá turma"}); // retornar json

            })
            //servidor escutar alguma porta
            server.listen(3000);
        
 6. Tipos de parametros enviados
    - query params = ?teste=1
    - route params = /users/1
    - Request body = {'nome':"fabbio", "idade":1}
    
 7. Rotas com query params
  
          server.get('/queryparams', (req,res) => {
          const nome = req.query.nome;
          return res.json({mensagem: `olá ${nome}`}); // retornar json
          })
          Navegador http://localhost:3000/queryparams?nome=fabbio
          
 8. Rotas com route params
 
         server.get('/routers/:id', (req,res) => {
          const id = req.params.id;
          /* Desestruturando 
            const {id} = req.params;
          */
          return res.json({mensagem: `buscando a rota ${id}`}); // retornar json
        })
        Navegador http://localhost:3000/routers/1
        
9. Rotas body

        9.1 Baixar o (insomnia)[https://insomnia.rest/download/core/?&ref=]
        9.2 criar uma nova requisição no insomina
          newRequest -> "ListarRotas" tipo get
        9.3 Colocar na barra de endereço o caminho da request
        9.4 send
        

        
        
        
        
 
  
