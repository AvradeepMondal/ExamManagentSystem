# Exam Management System

A **microservices-based exam management platform** built using **Java, Spring Boot, Spring Security, JWT, MongoDB, Redis, and Spring Cloud**.

## 🏗️ Architecture

**
                              +------------------+
                              |      Client      |
                              |  Web / Mobile    |
                              +--------+---------+
                                       |
                                       v
                              +------------------+
                              |   API Gateway    |
                              |      :8080       |
                              +--------+---------+
                                       |
             +-------------------------+-------------------------+
             |            |             |            |           |
             v            v             v            v           v
       +-----------+ +-----------+ +-----------+ +-----------+ +-----------+
       |   Auth    | |   User    | |   Quiz    | |  Question | |  Result   |
       |  Service  | |  Service  | |  Service  | |  Service  | |  Service  |
       +-----------+ +-----------+ +-----+-----+ +-----+-----+ +-----------+
                                         |             |
                                         |             v
                                         |      +-------------+
                                         |      |  AI Service |
                                         |      +-------------+
                                         |
                         +---------------+---------------+
                         |                               |
                         v                               v
                  +-------------+                 +-------------+
                  |   MongoDB   |                 |    Redis    |
                  +-------------+                 +-------------+
**
                    +--------------------------------------+
                    |        Discovery Server (Eureka)     |
                    |                 :8761                |
                    +--------------------------------------+
                       ^       ^       ^       ^       ^
                       |       |       |       |       |
                       +-------+-------+-------+-------+
                               Service Registration
**

## 🧩 Microservices

| Service              | Repository                                                               |   Status   |
| :------------------- | :----------------------------------------------------------------------- | :--------: |
| **Discovery Server** | [discoverServerExm](https://github.com/AvradeepMondal/discoverServerExm) | 🟢 Active  |
| **API Gateway**      | *Coming Soon*                                                            | 🟡 Planned |
| **Auth Service**     | [auth-service](https://github.com/AvradeepMondal/auth-service-Exm)       | 🟢 Active  |
| **User Service**     | [user-service](https://github.com/AvradeepMondal/user-service-Exm)       | 🟢 Active  |
| **Quiz Service**     | *Coming Soon*                                                            | 🟡 Planned |
| **Question Service** | [question-service](https://github.com/AvradeepMondal/question-service)   | 🟢 Active  |
| **Result Service**   | *Coming Soon*                                                            | 🟡 Planned |
| **AI Service**       | [ai-service](https://github.com/AvradeepMondal/ai-service)               | 🟢 Active  |

## 🛠️ Technologies

* **Language:** Java
* **Framework:** Spring Boot
* **Security:** Spring Security, JWT
* **Microservices:** Spring Cloud, Eureka, OpenFeign
* **Data & Caching:** MongoDB, Redis
* **API:** REST APIs

## 🚧 Project Status

**Ongoing Development**

Individual microservices are being developed and integrated progressively.
