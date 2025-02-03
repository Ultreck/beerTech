# E-Commerce Microservices System

A scalable e-commerce platform built with NestJS microservices. The system includes three core services: **User**, **Product**, and **Order**, each running independently and communicating via REST APIs and message patterns.

## Features
- **User Service**: User registration, login, JWT authentication, and profile management.
- **Product Service**: Product listing, inventory management, and pricing.
- **Order Service**: Order creation, transaction handling, and inter-service communication.
- **Database Isolation**: Each service uses its own PostgreSQL database.
- **Message-Based Communication**: Async event handling (e.g., inventory updates) via TCP/RabbitMQ.

## Technologies Used
- **Backend**: NestJS (Node.js)
- **Databases**: PostgreSQL
- **Authentication**: JWT, bcrypt
- **Communication**: REST, TCP (NestJS microservices), RabbitMQ (optional)
- **Containerization**: Docker, Docker Compose
- **Tools**: TypeORM, Swagger (optional)

---

## Project Structure
my-microservices-app/
│── api-gateway/            # 🚀 New API Gateway
│   ├── src/
│   │   ├── auth/
│   │   │   ├── auth.controller.ts  
│   │   │   ├── auth.module.ts      
│   │   ├── products/
│   │   │   ├── products.controller.ts  
│   │   │   ├── products.module.ts      
│   │   ├── orders/
│   │   │   ├── orders.controller.ts    
│   │   │   ├── orders.module.ts        
│   │   ├── app.module.ts  # API Gateway Core Module
│   │   ├── main.ts        # Starts API Gateway
│   ├── package.json
│   ├── .env
│
│── user/           # 👤 User Microservice
│   ├── src/
│   │   ├── user.controller.ts  
│   │   ├── user.module.ts      
│   │   ├── user.service.ts      
│   │   ├── main.ts        # Starts User Microservice
│   ├── package.json
│   ├── .env
│
│── product/        # 🛍 Product Microservice
│   ├── src/
│   │   ├── product.controller.ts  
│   │   ├── product.module.ts      
│   │   ├── main.ts        # Starts Product Microservice
│   ├── package.json
│   ├── .env
│
│── order/          # 📦 Order Microservice
│   ├── src/
│   │   ├── order.controller.ts  
│   │   ├── order.module.ts      
│   │   ├── main.ts        # Starts Order Microservice
│   ├── package.json
│   ├── .env
│
│── docker-compose.yml       # (Optional: for containerized setup)
│── README.md



## Getting Started

### Prerequisites
- Node.js v18+
- PostgreSQL
- Docker (optional)
- NestJS CLI (`npm install -g @nestjs/cli`)

---

### Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/e-commerce-microservices.git
   cd e-commerce-microservices


## Project setup

```bash
$ createdb -U postgres user_db

#Create a .env file  for user in the root directory
USER_DB_HOST=localhost
USER_DB_PORT=5432
USER_DB_USERNAME=postgres
USER_DB_PASSWORD=your_password
USER_DB_DATABASE=user_db
JWT_SECRET=your_jwt_secret
```bash
$ npm install
```

## Compile and run the project

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Run tests

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Deployment

When you're ready to deploy your NestJS application to production, there are some key steps you can take to ensure it runs as efficiently as possible. Check out the [deployment documentation](https://docs.nestjs.com/deployment) for more information.

If you are looking for a cloud-based platform to deploy your NestJS application, check out [Mau](https://mau.nestjs.com), our official platform for deploying NestJS applications on AWS. Mau makes deployment straightforward and fast, requiring just a few simple steps:

```bash
$ npm install -g mau
$ mau deploy
```

With Mau, you can deploy your application in just a few clicks, allowing you to focus on building features rather than managing infrastructure.

## Resources

Check out a few resources that may come in handy when working with NestJS:

- Visit the [NestJS Documentation](https://docs.nestjs.com) to learn more about the framework.
- For questions and support, please visit our [Discord channel](https://discord.gg/G7Qnnhy).
- To dive deeper and get more hands-on experience, check out our official video [courses](https://courses.nestjs.com/).
- Deploy your application to AWS with the help of [NestJS Mau](https://mau.nestjs.com) in just a few clicks.
- Visualize your application graph and interact with the NestJS application in real-time using [NestJS Devtools](https://devtools.nestjs.com).
- Need help with your project (part-time to full-time)? Check out our official [enterprise support](https://enterprise.nestjs.com).
- To stay in the loop and get updates, follow us on [X](https://x.com/nestframework) and [LinkedIn](https://linkedin.com/company/nestjs).
- Looking for a job, or have a job to offer? Check out our official [Jobs board](https://jobs.nestjs.com).

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://twitter.com/kammysliwiec)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](https://github.com/nestjs/nest/blob/master/LICENSE).
