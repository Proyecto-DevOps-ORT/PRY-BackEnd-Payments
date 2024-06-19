# Payments Service Example

Este proyecto es un ejemplo de un servicio de pagos utilizando java y Docker.


## Construir imagen
```
docker build -t payments-service-example:1 .
```
## Crear contenedor
```
docker run --name payments-service-example-container -d  -p 8081:8080 payments-service-example:1
```
## Obtener Ip del contenedor
```
docker inspect payments-service-example-container
```  
=> IPAddress": "172.17.0.2"


### Verificacion de app en POSTMAN

- Request tipe: POST
- URL: http://localhost:8081/payments/123

    Resultado:
    ```
    {
        "orderId": "123",
        "success": false,
        "description": "No money."
    }
    ```


