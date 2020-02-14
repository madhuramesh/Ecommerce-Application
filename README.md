# Ecommerce-Application
Ecom - Online checkout using Microservices SpringBoot JPA and Maven

PI360 Microservices

java version "10.0.2"
Maven 3.5.4

Java -jar target/PI360Item-0.0.1-SNAPSHOT.jar
Java -jar -Dserver.port=9090 target/PI360Inventory-0.0.1-SNAPSHOT.jar
Java -jar -Dserver.port=9093 target/PI360Order-0.0.1-SNAPSHOT.jar
Java -jar -Dserver.port=9091 target/PI360Cart-0.0.1-SNAPSHOT.jar
Java -jar -Dserver.port=9092 target/PI360CheckOut-0.0.1-SNAPSHOT.jar


Get - http://localhost:8080/item
Get - http://localhost:9090/inventory
Get - http://localhost:9091/cart/madhu
Get - http://localhost:9092/checkout/madhu/items

Inventory(Post/Put)

Mvn install
Java -jar -Dserver.port=9090 target/PI360Inventory-0.0.1-SNAPSHOT.jar


{
    "id": 1,
    "itemName": "Black Back pack",
    "qty": 1000
}

Item

Mvn install
Java -jar target/PI360Item-0.0.1-SNAPSHOT.jar

Cart(Post/Put/Delete/Get)

Mvn install
Java -jar -Dserver.port=9091 target/PI360Cart-0.0.1-SNAPSHOT.jar

{
       "custName":"swara",
        "itemName": "Black Back pack",
        "qty": 1
    }

CheckOut(Post/Get)

Mvn install
Java -jar -Dserver.port=9092 target/PI360CheckOut-0.0.1-SNAPSHOT.jar

{
       "custAddr":"9811 NE 16th St"
       
    }

Order(Post/Get)

Mvn install
Java -jar -Dserver.port=9093 target/PI360Order-0.0.1-SNAPSHOT.jar


 {
        "id": 1,
        "itemName": "Black Back pack",
        "custName": "swara",
        "qty": 1,
        "shippingAddr": "9811 NE 16th St",
        "creditCheck": true
    }
