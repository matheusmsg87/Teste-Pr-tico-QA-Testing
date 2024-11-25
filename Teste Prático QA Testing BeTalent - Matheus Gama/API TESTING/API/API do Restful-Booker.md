# Relatório de execução dos testes da API Restful-Booker

## Cenários Testados

## 1. Autenticação
### 1.1 Gerar token de autenticação
- **Endpoint:** `POST /auth`
- **Request:**
  ```json
  {
    "username": "admin",
    "password": "password123"
  }
  ```
- **Resposta Esperada:**
  - **Status Code:** `200 OK`
  - **Body:** Contém o campo `token`.
- **Resultado Obtido:**
  - **Status Code:** `200 OK`
  - **Body:**
  ```json
  {
    "token": "df8eac3b81b6042"
  }
  ```

### 1.2 Tentar gerar token com credenciais inválidas
- **Endpoint:** `POST /auth`
- **Request:**
  ```json
  {
    "username" : "matheus",
    "password" : "password"
  }
  ```

- **Resposta Esperada:**
  - **Status Code:** `200 OK`
  - **Body:** `{ "reason": "Bad credentials" }`


- **Resultado Obtido:**
  - **Status Code:** `200 OK`
  - **Body:**
  ```json
  {
    "reason": "Bad credentials"
  }
  ```

---

## 2. Gestão de Reservas

### 2.1 Criar uma nova reserva 
- **Endpoint:** `POST /booking`
- **Request:**
  ```json
  {
    "firstname" : "matheus",
    "lastname" : "silva",
    "totalprice" : 400,
    "depositpaid" : true,
    "bookingdates" : {
        "checkin" : "2025-10-03",
        "checkout" : "2025-10-23"
    },
    "additionalneeds" : "Breakfast"
  }
  ```
- **Resposta Esperada:**
  - **Status Code:** `200 OK`
  - **Body:** Contém o campo *bookingid* id único.
- **Resultado Obtido:**
  - Reserva criada com sucesso.
  - **Status Code:** `200 OK`
  - **Body:**
  ```json
  {
    "bookingid": 2188,
    "booking": {
        "firstname": "matheus",
        "lastname": "silva",
        "totalprice": 400,
        "depositpaid": true,
        "bookingdates": {
            "checkin": "2025-10-03",
            "checkout": "2025-10-23"
        },
        "additionalneeds": "Breakfast"
    }
  ```
  

### 2.2 Buscar uma reserva específica
- **Endpoint:** `GET /booking/{id}`
- **Resposta Esperada:**
  - **Status Code:** `200 OK`
  - **Body:** Fornecer o "id" da reserva que deseja buscar.
- **Resultado Obtido:**
  - Reserva recuperada com sucesso.
  - **Status Code:** `200 OK`
  - **Body:**
  ```json
    {
    "firstname": "matheus",
    "lastname": "silva",
    "totalprice": 400,
    "depositpaid": true,
    "bookingdates": {
        "checkin": "2025-10-03",
        "checkout": "2025-10-23"
    },
    "additionalneeds": "Breakfast"
    }
  ```


### 2.3 Listar todas as reservas
- **Endpoint:** `GET /booking`
- **Resposta Esperada:**
  - **Status Code:** `200 OK`
  - **Body:** Lista de todas as reservas.


- **Resultado Obtido:**
  - Todas as reservas listadas com sucesso.
  - **Status Code:** `200 OK`
  - **Body:**
  ```json
    {
        {
        "bookingid": 267
    },
    {
        "bookingid": 2750
    },
    {
        "bookingid": 2719
    },
    {
        "bookingid": 2076
    },
    {
        "bookingid": 3488
    },
    {
        "bookingid": 741
    },
    {
        "bookingid": 1345
    }
    }
  ```


### 2.4 Atualizar uma reserva existente
- **Endpoint:** `PUT /booking/{id}`
- **Request:**
  ```json
  {
    "firstname" : "matheus",
    "lastname" : "Gama",
    "totalprice" : 400,
    "depositpaid" : true,
    "bookingdates" : {
        "checkin" : "2025-10-03",
        "checkout" : "2025-10-23"
    },
    "additionalneeds" : "café da manhã"
  }
  ```
- **Headers:** `Cookie: token={{token}}`
- **Resposta Esperada:**
  - **Status Code:** `200 OK`
  - **Body:** Informações atualizados da reserva.

- **Resultado Obtido:**
  - Reserva atualizada com sucesso.
  - **Status Code:** `200 OK`
   - **Body:**
  ```json
  {
    "firstname": "matheus",
    "lastname": "Gama",
    "totalprice": 400,
    "depositpaid": true,
    "bookingdates": {
        "checkin": "2025-10-03",
        "checkout": "2025-10-23"
    },
    "additionalneeds": "café da manhã"
  }
  ```

### 2.5 Deletar uma reserva
- **Endpoint:** `DELETE /booking/{id}`
- **Headers:** `Cookie: token={{token}}`
- **Resposta Esperada:**
  - Reserva deletada
  - **Status Code:** `201 Created`
- **Resultado Obtido:**

  - Reserva deletada com sucesso.
  - **Status Code:** `201 Created`
   - **Body:**
  ```json
    Created
  ```
---









## 3. Filtros e Buscas
### 3.1 Buscar reservas por nome
- **Endpoint:** `GET /booking?firstname=matheus`
- **Resposta Esperada:**
  - **Status Code:** `200 OK`
  - **Body:** Lista de reservas com o nome "matheus".
- **Resultado Obtido:**

  - Filtro funcionou conforme o esperado retornando o id conforme o nome.
  - **Status Code:** `200 OK`
   - **Body:**
  ```json
  {
    {
        "bookingid": 208
    }   
  }
  ```


### 3.2 Buscar reservas por data de check-in
- **Endpoint:** `GET /booking?checkin=2024-10-03`
- **Resposta Esperada:**
  - **Status Code:** `200 OK`
  - **Body:** Lista de reservas com check-in em "2024-10-03".

- **Resultado Obtido:**
  - Busca realizada com sucesso.
  - **Status Code:** `200 OK`
  - **Body:**
  ```json
  {
    {
        "bookingid": 1710
    },
    {
        "bookingid": 2384
    },
    {
        "bookingid": 1981
    },
    {
        "bookingid": 2404
    },
    {
        "bookingid": 223
    },
    {
        "bookingid": 191
    }
  }
  ```


### 3.3 Buscar reservas por data de check-out
- **Endpoint:** `GET /booking?checkout=2024-10-23`
- **Resposta Esperada:**
  - **Status Code:** `200 OK`
  - **Body:** Lista de reservas com check-out em "2024-10-23".

- **Resultado Obtido:**
  - Busca realizada com sucesso.
  - Busca realizada com sucesso.
  - **Status Code:** `200 OK`
  - **Body:**
  ```json
  {
    {
        "bookingid": 1876
    },
    {
        "bookingid": 610
    },
    {
        "bookingid": 1980
    },
    {
        "bookingid": 1151
    },
    {
        "bookingid": 478
    },
    {
        "bookingid": 3687
    }
  }
  ```

---

## Resumo

- Todos os endpoints funcionaram conforme esperado.
- os Header foram validadas corretamente.
- Gestão de reservas apresentou resultados consistentes com os cenários propostos.

## Bugs Encontrados
- **Nenhum bug identificado durante a execução dos testes.**



