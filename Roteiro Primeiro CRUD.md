# Primeiro CRUD
 
- CREATE
- READ
- UPDATE
- DELETE

1. Abrir o VSCode

2. Criar uma pasta 
  PrimeiraAplicação
  
3. Criar o arquivo package json
  yarn init -y
  
4. Instalar a dependencia Express
  yarn add express

5. criar o arquivo index.js
          const express = require('express');

          const server = express(); //chamar a função express

          server.use(express.json()); //informar ao express que recebo json

          const users = ["Jose", "Pedro", "Carlos"];

          server.get('/users/:index', (req,res) => {
            const {index} = req.params;
            return res.json(users[index]); 
          })

          server.get('/users', (req,res) => {
            return res.json(users); 
          })

          server.post('/users', (req,res) => {
            const {nome} = req.body;
            users.push(nome);
            return res.json(users); 
          })

          server.put('/users/:index', (req,res) => {
            const {nome} = req.body;
            const {index} = req.params;
            users[index] = nome;
            return res.json(users); 
          })

          server.delete('/users/:index', (req,res) => {
            const {index} = req.params;
            users.splice(index, 1); //deleta tantas posições a partir do index
            //return res.json(users); 
            return res.send();
          })
          
   6.middleware
            função que recebe os parametros req e res e outros parametros e manipula esses parametros
            
            middleware global: não importa arota que eu acessar o middleware sempre vai ser acessada
            
                server.use((req,res, next) => {
                console.time('Request');
                //console.log("A requisição foi chamada");
                console.log(`Método: ${req.method}; URL: ${req.url}`);
                //return next();

                next();

                console.log("Finalizou");
                console.timeEnd('Request');
              })
              
          middleware local 
          
            Verificar se a requisição tem o parametro de nome
              function checarUsuarioExiste (req, res, next){
                if(!req.body.nome){
                  return res.status(400).json({erro: "Usuario não informado no corpo da requisição"})
                }

                return next();
              }


              server.post('/users', checarUsuarioExiste, (req,res) => {
                const {nome} = req.body;
                users.push(nome);
                return res.json(users); 
              })

              server.put('/users/:index', checarUsuarioExiste, (req,res) => {
                const {nome} = req.body;
                const {index} = req.params;
                users[index] = nome;
                return res.json(users); 
              })
            
            Verificar se o usuario existe de acordo com o index
            
                function checarIndexArray(req, res, next){
                  if(!users[req.params.index]){
                    return res.status(400).json({erro: "Usuario não existe"})
                  }
                  return next();
                }
                
               server.get('/users/:index',checarIndexArray, (req,res) => {
                const {index} = req.params;
                return res.json(users[index]); 
              })
              
              server.put('/users/:index', checarUsuarioExiste, checarIndexArray, (req,res) => {
                const {nome} = req.body;
                const {index} = req.params;
                users[index] = nome;
                return res.json(users); 
              })
              
              server.delete('/users/:index',checarIndexArray, (req,res) => {
                const {index} = req.params;
                users.splice(index, 1); //deleta tantas posições a partir do index
                //return res.json(users); 
                return res.send();
              })


              
          
     
