# Projeto Final - Módulo 3

## API RESTful

## Introdução

Projeto final que consiste em criar uma API que contenha todo o CRUD, em 5 rotas distintas, sobre o tema Pokémon (escolhido pelos autores), as quais são:

- `/add` - para adicionar itens ao banco de dados;

- `/update` - para atualizar itens ao banco de dados;

- `/listall` - para listar todos os itens do DB;

- `/listid` - para listar através de um id específico;

- `/delete` - para apagar qualquer item do DB.

  

## Preparação para utilizar a API

Antes de usarmos nossa API, é necessário que tenha o software Node Js instalado no seu computador.

Para isso, acesse o link https://nodejs.org/en/ e obtenha a versão correta do Node para seu sistema operacional. Siga todas as orientações conforme cada tela do processo de instalação.

Com o Node Js devidamente instalado, baixe ou clone as pastas deste repositório e salve em seu computador.

Após ter os arquivos da API salvos em seu computador, abra o Prompt de comando/terminal (CMD) do seu sistema operacional, vá até a pasta onde os arquivos da API estão e inicialize os comandos abaixo:

```javascript
npm init
npm start
npm install dotenv
npm install express --save
npm install mongoose
npm install express-validator
```

Feito as instalações das dependências que são necessárias para o correto funcionamento do Back-end, será necessário também instalar as dependências em relação a parte do Front-end, conforme comandos via Prompt de comando (estando da mesma forma na pasta com os arquivos do Front-end):

```javascript
npm install yarn
yarn install
yarn start
```

Se o package manager ```yarn``` não funcionar, usar:

```javascript
npm install
npm start
```



## Utilizando a API via Front-end ##

Com todas as dependências instaladas e os servidores funcionando, você pode navegar através da página que abriu ao inicializar o Front-end, podendo cadastrar, atualizar, listar ou deletar qualquer pokémon que quiser.



## Utilizando a API via Postman/Insomnia/Thunder Client ##

Caso não queira utilizar a aplicação com o Front disponibilizado, é possível utilizar aplicações como Postman, software como Insomnia ou extensões como Thunder Client, no VS Code.



![postman](C:\Users\User\Documents\Curso_Programacao_pela_Blue\Codigos\MODULO_3\BackM3ProjFinal\img\postman.png)

![insomnia](C:\Users\User\Documents\Curso_Programacao_pela_Blue\Codigos\MODULO_3\BackM3ProjFinal\img\insomnia.png)

![thunderclient](C:\Users\User\Documents\Curso_Programacao_pela_Blue\Codigos\MODULO_3\BackM3ProjFinal\img\thunderclient.png)

Para utilizar o Postman, você irá precisar acessar o link https://www.postman.com/ e criar uma conta ou, se preferir, baixar o software neste link aqui: https://www.postman.com/downloads/. Para mais detalhes de como utilizar essa aplicação, acesse https://learning.postman.com/docs/getting-started/introduction/.

O mesmo se aplica ao Insomnia; o link para download: https://insomnia.rest/download e o link para consultar a documentação para melhor entender seu funcionamento: https://docs.insomnia.rest/.

Já em relação ao Thunder, ele é uma extensão do VS Code, então, para utiliza-lá, vá até a aba Extensions (ou Extensão, se seu VS Code estiver em português) e digite "Thunder Client", provavelmente será a primeira opção da listagem. Clique no banner com o nome da extensão e irá aparecer uma janela, igual a última imagem de exemplo acima. Clique em Install (ou Instalar) e após instalar, clique em Able (caso já não esteja habilitado após a instalação). Pronto, já está pronto para testar nossa API.

### As Rotas

- A rota ***/add*** adiciona um novo pokémon ao  banco de dados. Para isso, precisa preencher os dados conforme o exemplo abaixo:

  ```json
   {
   	"nome": "Blastoise",
      "peso": 235,
      "altura": 2,
      "imagemUrl": "https://www.pokemon.com.br",
      "regiao": "Johto"
    }
  ```

- A rota ***/update/*** atualiza, por meio do Id do item cadastrado, os dados. Ao usar a rota ***/listall*** tem-se o id logo no início do cadastro.

  ```json
  {
    "_id": "618b1f93b8bc900c4e773901",
    "nome": "Pikachu",
     "peso": 15,
     "altura": 1,
     "imagemUrl": "https://www.pokemon.com.br",
     "regiao": "Johto"
  }
  ```

  

- A rota ***/listall***  são responsáveis por listar na tela todos os pokémons cadastrados no banco de dados.

  Ao passar os parâmetros URL onde está rodando a aplicação (no caso, via Heroku), a rota principal (que é ou ***/agua***, ***/grass***, ***ghost***, ***/psiquico*** ou ***/fogo***) e a subrota a qual quer acessar (***/listall*** nesse caso), irá retornar todos os dados cadastrados no banco de dados, conforme exemplo abaixo:

  ```json
   {
      "_id": "618b1577d6154770799c1926",
      "nome": "Wartotle",
      "peso": 25,
      "altura": 1.5,
      "imagemUrl": "https://www.pokemon.com.br",
      "regiao": "Johto"
    }
  ```

  

- A rota ***/listid/*** irão retornar um cadastro especifico, bastando colocar o id do pokémon cadastrado, após o último "/".

- A rota ***/delete/*** irá excluir o cadastro. Assim como a rota ***/update***, é necessário informar o id após o "/" para a API identificar qual cadastro deve excluir.

Se você estiver utilizando o Thunder Client, no repositório tem disponível as Collections (que são espécies de atalhos para evitar estar escrevendo as rotas todas as vezes) de cada rota, para facilitar a utilização delas. Basta importar as Collections (que estão salvas com arquivos .JSON) e as rotas principais estão separadas por pastas, cada pasta contém as 5 rotas do CRUD.

Caso utilize o POSTMAN ou Insomnia, o link do projeto para utilizar a API é https://backm3final.herokuapp.com/.



