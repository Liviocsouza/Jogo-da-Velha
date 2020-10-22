# Jogo-da-Velha
Hackenge de Engenharia de Software da Universidade Federal de Pernambuco do Curso de Sistemas da informação 2020.
Criação da arquitetura da API de um jogo da velha feito em Node e Express.

## Equipe 
 - Josenildo lopes (jls2)
 - Livio Cavalcanti de souza (lcs9)
 - Yves Lawrrence Silva de Andrade Cavalcante (ylsa)

## Method HTTP

**GET /StartGame**
  - Metodo para criar uma sala randomicamente
    - Exemplo de envio json: {"Id":123 , "Nome": "livio", "Vitorias": 0, "Derrotas": 0, "Empate": 0 ,"Board":[]}
    
 **GET /OpenGame**
  - Metodo para entrar em uma sala já existente
    - Exemplo de envio json: {"SalaId": "0131das1dasd"}
 
**Post /Sing-in**
  - Cadastrar usuario
    - Exemplo de envio json: {"Id":123 , "Nome": "livio", "Senha":"das1d23"}
    - Exceção: Informações invalidas/Insuficiente
  
**POST/Login**
 - Verifica se o usuario está cadastrado e faz o login no sistema
    - Exemplo de envio json: {"Id":123, "Nome": "livio", "Senha":"das1d23"}
    - Exceção: Usuario Invalido
 
 **Put/Resultado** 
- Verifica qual resultado do jogo
  - Exemplo de envio json: {"Id":123, "Nome": "livio", "Vitorias": 0, "Derrotas": 0, "Empate": 0 ,"Board":[[X,X,X],[X,0,0][0,X,0]]}
  - Exceção: Informações Insuficiente 

**Delete/RemoverUsuario**
 -  Deletar usuario cadastro
     - Exemplo de envio json: {"Id":123, "Nome": "livio", "Senha":"das1d23"}
     - Exceção: Usuario não cadastrado
     
**POST /Logout**
 - Faz o logout do sistema, finalizando a conexão
  - Exemplo de envio json: {"Id":123 , "Nome": "livio", "Senha":"das1d23"}
  
 **GET /Ranking**
  - Listar a pontuação do jogador que tiver maior numero de vitoria
  
  **GET /Ranking/invicto**
   - Lista somentes os jogadores invictos e quantidade de partidas invictos
   
  **PUT /SalvarGame**
   - Ao finalizar o jogo ele ira  salvor o resultado no Banco de Dados, Atualizando o ranking
  
  
  
