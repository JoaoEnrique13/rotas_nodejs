# App.js
```js
const express = require('express')
const app = express()

//Callback - cria um servidor web
app.listen(8081, function(){
    console.log("Servidor rodando na porta 8081");
})

//home
app.get('/', function(req, res){
    res.sendFile(__dirname + '/html/index.html')
})

//cadastrar produto
app.get('/cadastrar/produto', function(req, res){
    res.sendFile(__dirname + '/html/cadastrar_produto.html')
})

//pesquisar produto
app.get('/pesquisar/produto/modelo', function(req, res){
    res.sendFile(__dirname + '/html/pesquisar_produto.html')
})

//contato produto
app.get('/contato/sac/produto', function(req, res){
    res.sendFile(__dirname + '/html/contato.html')
})
