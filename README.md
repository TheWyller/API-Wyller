# Documentação da Api

## Registrar Usuário:

### POST/register

         {
            "email": "wyller@mail.com",
            "password": "123456",
            "firstname":"Wyller",
            "lastname": "Fernandes",
            "age": 29
          }

## Logar Usuário:

### POST/login

          {
            "email": "wyller@mail.com",
            "password": "123456"
          }

---

## Ver seu próprio Usuario:

\*deve estar logado

    GET/users/:id-do-user

---

## Cadastrar item:

\*deve estar logado - será visto por todos, mas só o dono pode editar

### POST/itens

          {
            "userId": 2,
            "type":"Eletronico",
            "name":"Computador",
            "url_img":"https://s2.glbimg.com/4J1KP8B8..."
          }

## Cadastrar item:

\*deve estar logado - será visto por todos que estiverem logados, mas só o dono pode editar

### POST/info

          {
            "userId": 2,
            "UserName":
            "Leganza",
            "url_img":"https://upload.wikimedia.org/wikipe...",
          }

---

## Visualizar todos os itens:

    GET/itens

## Visualizar um os itens:

    GET/itens/:id-do-item

---

## Visualizar todas as info:

    GET/info

## Visualizar uma info:

\*apenas o dono da info poder usar essa rota

    GET/info/:id-do-info

---

## Modificar um os itens:

\*apenas o dono do item poder usar essa rota (pode ser um ou vários atributos)

### PATCH/itens/:id-do-item

          {
            "userId": 2,
            "type":"Eletronico222222"
          }

## Modificar uma info:

\*apenas o dono do item poder usar essa rota (pode ser um ou vários atributos)

### PATCH/info/:id-do-info

          {
            "userId": 2,
            "UserName": "Leganzaaaaa"
          }

---

## Deletar um dos itens

\*apenas o dono do item poder usar essa rota

    DELETE/itens/:id-do-item

## Deletar uma info

\*apenas o dono do item poder usar essa rota

    DELETE/info/:id-do-info
