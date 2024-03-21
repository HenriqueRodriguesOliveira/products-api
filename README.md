<div align="center">
 <h1>Products API</h1>
</div>
  <img src="https://github.com/HenriqueRodriguesOliveira/products-api/assets/79226722/a96ea33d-70ef-4e46-8521-b88ea2fcd72e" alt="Logo Java">
</br>
</br>

## Sobre o Projeto
> O Products-API é uma API RESTful, com base no método do Leonard Richardson para padronizar
e facilitar o desenvolvimento APIs Rest, aonde ele aplica as 4 regras: POX, Resourses, Verbos HTTP e Hateos.

Neste projeto eu desenvolvi códigos com relação aos estudos do SpringBoot.
- [x] Controller
- [x] Models
- [x] Repositories
- [x] DTO
- [x] JPA

## Requisitos
 * IDE de sua escolha(VScode / Eclipse / IntelliJ).
 * Java 17
 * Maven
 * Postman
 * [Guia de configuração de ambiente.](https://spring.io/quickstart)

## Instalação
1. Copie o link do projeto que está no Github.
2. Instale o Git.
3. No CMD digite git LinkDoProjetoGithub.
4. Configure a sua máquina de acordo com os requisitos solicitado acima.

## Comandos
Requisições para a API devem seguir os padrões:
| Métodos | Descrição |
| --- | --- |
| `GET` | Retorna informações de um ou mais registros. |
| `POST` | Utilizado para criar um novo registro. |
| `PUT` | Atualiza dados de um registro ou altera sua situação. |
| `DELETE` | Remove um registro do sistema. |

## Respostas
| Código | Descrição |
|---|---|
| `200` | Requisição executada com sucesso (success).|
| `400` | Erros de validação ou os campos informados não existem no sistema.|
| `401` | Dados de acesso inválidos.|
| `404` | Registro pesquisado não encontrado (Not found).|
| `405` | Método não implementado.|
| `410` | Registro pesquisado foi apagado do sistema e não esta mais disponível.|
| `422` | Dados informados estão fora do escopo definido para o campo.|
| `429` | Número máximo de requisições atingido. (*aguarde alguns segundos e tente novamente*)|

## Listar
As ações de listar permitem o envio dos seguintes parâmetros:

| Parâmetro | Descrição |
| --- | --- |
| `filtro` | Filtra dados pelo valor informado. |
| `page` | Informa qual página deve ser retornada. |

## Dados
### Listar [GET ALL /products]
Buscar todas as informações da API

+ Request (application/json)

    + Params

        | Key | Value |
        | --- | --- |
        | page | 1 |
        | size | 10 |
        | sort | idProduto, desc |


+ Response 200 (application/json)
  
  ```
  "idProduct": "46057a81-1a49-4286-be5b-cff84d5bdfc1",
  "name": "Monitor Dell 27 ATUALIZADO",
  "value": 5500.00,
  "links": []
  ```

### Listar [GET ONE /products]
Buscar uma informação específica da API


+ Request (application/json)

    ```products/{id}```
        

+ Response 200 (application/json)
  
  ```
  "idProduct": "46057a81-1a49-4286-be5b-cff84d5bdfc1",
  "name": "Monitor Dell 27 ATUALIZADO",
  "value": 5500.00,
  "links": []
  ```

### Adicionar [POST /products]
Adicionar um produto na API

+ Request (application/json)

    + Body
        ```
        {
           "name": "Lavadora LG",
            "value": 3500.00
        }
        ```
        

+ Response 201 (application/json)
  
  ```
  {
    "idProduct": "f9bcf754-6413-4218-9afe-19a719d824b1",
    "name": "Lavadora LG",
    "value": 3500.00
  }
  ```

### Adicionar [PUT /products/{id}]
Atualizar um produto todas da API

+ Request (application/json)

    + Body
        ```
        {
           "name": "Lavadora LG ATUALIZADA",
            "value": 4000.00
        }
        ```
        

+ Response 200 (application/json)
  
  ```
  {
    "idProduct": "a0e935a1-b2e5-41f4-8c5a-561992bc0542",
    "name": "Lavadora LG ATUALIZADA",
    "value": 2000.00
  }
  ```

### Adicionar [DELETE /products/{id}]
Deletar um produto da API

+ Request (application/json)
  
         application/{id}
  
        

+ Response 200 (application/json)
  
  ```
    Product deleted successfully.
  ```

> [!CAUTION]
> Caso deseje cadastrar algum produto incompleto, ele não será registrado.

## Fontes
* [Roadmap de Java](https://roadmap.sh/java)
* [Curso Spring Boot 3](https://www.youtube.com/watch?v=wlYvA2b1BWI)

## Licença
This project is licensed under the MIT License - see the [LICENSE](https://opensource.org/licenses/MIT) page for details.
