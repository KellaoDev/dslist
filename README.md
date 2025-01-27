## DsList

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/KellaoDev)
# About project 

This RESTful API was developed with Java and uses the Spring Boot framework. The API has the functionality to load games, list games by ID, display game categories, and manipulate the position of games within categories.

## API documentation

#### Get games

```http
  GET {LOCALHOST}/games
``` 

#### Get games by id

```http
  GET {LOCALHOST}/games/{id}
```

#### Get list

```http
  GET {LOCALHOST}/list
```

#### Get games by lists

```http
  GET {LOCALHOST}/lists/{id}/games
```

#### Update game position in list

```http
  POST {LOCALHOST}/lists/{id}/replacement
```

| Field   | Type       | Required                                   |  allowed values| 
| :---------- | :--------- | :------------------------------------------ | :------|
| `sourceIndex`      | `integer (int64)` | **Yes** | Bearer eyJhbGciOiJIUzI1Ni... **()** |
| `destinationIndex`      | `integer (int64)` | **Yes** |  >= 0 |

## Technologies used

#### • Java
#### • Spring Framework
#### • H2 / PostgreSQL / Hibernate
#### • Docker / WSL

## How to execute the project

### Prerequisites:


#### Make sure you have installed:

JDK 17 → java -version

Maven → mvn -version

Database Test (H2)

Database Production(PostgreSQL)

Docker e WSL


```bash
# Clone repository
https://github.com/KellaoDev/dslist

# Configure database test
In the archive application.properties:
Example(H2)

spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true

# Configure database
In the archive application.properties:
Example(PostgreSQL)

spring.datasource.url=jdbc:postgresql://localhost:5432/your_database
spring.datasource.username=your_username
spring.datasource.password=your_password

# Run the project with Maven
mvn spring-boot:run

# Access the API
http://localhost:8080 (or another configured port)
```
## Author

### Kélio Cirilo da Silva Filho
https://www.linkedin.com/in/keliocirilo/



