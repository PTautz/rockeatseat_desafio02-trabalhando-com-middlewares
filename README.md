## DESAFIO 02 - Rockeatseat

Nesse desafio você irá trabalhar mais a fundo com middlewares no Express. Dessa forma você será capaz de fixar mais ainda os conhecimentos obtidos até agora. 

Para facilitar um pouco mais do conhecimento da regra de negócio, você irá trabalhar com a mesma aplicação do desafio anterior: uma aplicação para gerenciar tarefas (ou *todos*) mas com algumas mudanças.

Será permitida a criação de um usuário com `name` e `username`, bem como fazer o CRUD de *todos*:

- Criar um novo *todo*;
- Listar todos os *todos*;
- Alterar o `title` e `deadline` de um *todo* existente;
- Marcar um *todo* como feito;
- Excluir um *todo*;

Tudo isso para cada usuário em específico. Além disso, dessa vez teremos um plano grátis onde o usuário só pode criar até dez *todos* e um plano Pro que irá permitir criar *todos* ilimitados, isso tudo usando middlewares para fazer as validações necessárias.

A seguir veremos com mais detalhes o que e como precisa ser feito 🚀

## Middlewares 

### Requisitos

- [x] Deve ser possível encontrar usuário pelo username e acessá-lo pelo `request.user`
- [x] Deve ser possível ao usuário do plano `free` criar 10 tarefas.
- [x] Deve ser possível ao usuário do plano `pro` criar tarefas infinitamente.
- [x] Deve ser possível colocar usuário e tarefa na requisição se ambos existirem.
- [x] Deve ser possível encontrar usuário pelo id da rota e passá-lo para o `request.user`


## regras de testes

  - [x] Não deve ser possível encontrar um usuário não existente
  - [x] Não deve ser possível cadastrar nova tarefa caso o usuário não for plano `pro` e já possuir 10 tarefas cadastradas
  - [x] Não deve ser possível colocar usuário e tarefa na requisição se usuário não existe.
  - [x] Não deve ser possível colocar usuário e tarefa na requisição se tarefa não existe.
  - [x] Não deve ser possível colocar usuário e tarefa na requisição quando a id da tarefa não for única
  - [x] Não deve ser possível passar usuário para `request.use` quando o usuário não existe.