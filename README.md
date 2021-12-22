
# Sobre o projeto

## Front-End

* Construir uma tela de login com alta disponibilidade e o usuário deve permanecer logado.
* Criar um menu para o usuário navegar nas telas do sistema
* Construir um CRUD de anúncios (listagem, criação, atualização e deleção)
* Construir um CRUD de marcas (listagem, criação, atualização e deleção)
* Construir um CRUD de categorias (listagem, criação, atualização e deleção)
* Construir um CRUD de atributos (listagem, criação, atualização e deleção)
* Utilizar algum framework de Javascript (React, Vue ou Angular)
* Utilizar algum serviço de CDN
* Utilizar o S3 da Amazon para salvar os arquivos estaticos
* Utilizar um dominio HTTPS

## Back-End

* Criar um serviço de anúncios
* Criar um serviço de preço
* Criar um serviço de estoque
* Criar um serviço de autorização/autenticação utilizando o serviço Keycloak 
* Utilizar Java ou Kotlin como linguagem principal
* Utilizar a última versão do Spring como framework web
* Criar um serviço como Gateway utlizando o Spring Cloud
* Utlizar rate limit no serviço Gateway
* Utlizar o MongoDb nas aplicações de preço e estoque
* Utlizar o PostgreSQL na aplicação de produto
* Utilizar o Kafka ou Amazon SQS para a comunicação entre microsserviços
* Utlizar o Redis como cache distribuido nas consultas
* Criar teste unitários com cobertura de mais de 80%
* Criar testes integrados
* Criar uma documentação utilizando o Swagger

## DevOps

* Utlizar o Kubernetes para gerenciamento dos serviços
* Garantir o auto escalonamento das aplicações
* Garantir a resiliência das aplicações
* Utilizar o Nginx como LoadBalancer
* Fazer deploy de todas as aplicações no EC2 da Amazon


## Referência API

#### Criar Marca

```http
  POST /brands
```

| Parâmetro | Tipo     | Descrição                |
| :-------- | :------- | :------------------------- |
| `title` | `String` |  |
| `description` | `String` |  |

#### Criar Atributo

```http
  POST /attributes
```

| Parâmetro | Tipo     | Descrição                |
| :-------- | :------- | :------------------------- |
| `title` | `String` |  |
| `description` | `String` |  |

#### Criar Categoria

```http
  POST /categories
```

| Parâmetro | Tipo     | Descrição                |
| :-------- | :------- | :------------------------- |
| `title` | `String` |  |
| `description` | `String` |  |

#### Criar Anúncio

```http
  POST /ads
```

| Parâmetro | Tipo     | Descrição                |
| :-------- | :------- | :------------------------- |
| `title` | `String` |  |
| `description` | `String` |  |
| `brand` | `String` |  |
| `category` | `String` |  |
| `attributes` | `String[]` |  |


#### Criar Preço

```http
  POST /prices
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `adId`      | `string` | Id do anúncio |
| `value`      | `double` | Valor do preço |


```http
  POST /stocks
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `adId`      | `string` | Id do anúncio |
| `value`      | `int` | Valor do estoque |



