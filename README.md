# bestbuy-cloud-native-app


## Architecture Diagram

```mermaid
flowchart LR
    subgraph Users
        C[Customer]
        E[Employee / Admin]
    end

    subgraph Frontend Applications
        SF[Store-Front]
        SA[Store-Admin]
    end

    subgraph Microservices
        PS[Product-Service]
        OS[Order-Service]
        ML[Makeline-Service]
        IC[Inventory-Consumer]
    end

    subgraph Messaging
        MQ[RabbitMQ]
    end

    subgraph Database
        DB[(MongoDB)]
    end

    C --> SF
    E --> SA

    SF --> PS
    SF --> OS
    SA --> PS
    SA --> OS

    OS --> DB
    OS --> MQ

    MQ --> ML
    MQ --> IC

    ML --> DB
    IC --> PS
    PS --> DB
```
```

## bestbuy-store-front
https://github.com/Jingjing-Duan/bestbuy-store-front

## bestbuy-store-admin
https://github.com/Jingjing-Duan/bestbuy-store-admin


## bestbuy-product-service
https://github.com/Jingjing-Duan/bestbuy-product-service


## bestbuy-inventory-consumer
https://github.com/Jingjing-Duan/bestbuy-inventory-consumer


## bestbuy-order-service
https://github.com/Jingjing-Duan/bestbuy-order-service


## bestbuy-makeline-service
https://github.com/Jingjing-Duan/bestbuy-makeline-service


## bestbuy-cloud-deployment
https://github.com/Jingjing-Duan/bestbuy-cloud-deployment





