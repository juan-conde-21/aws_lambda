# AWS API Gateway ---> Lambda ---> DynamoDB 

1. Crear la tabla "product-inventory" en DynamoDB con el partition key "productId"

![image](https://github.com/juan-conde-21/aws_lambda/assets/13276404/122b4d73-b45a-4edb-bece-f02e9dc9af7c)

![image](https://github.com/juan-conde-21/aws_lambda/assets/13276404/4ea63c6d-2879-41cf-904c-a5b5fa1343c8)

2. Crear una funcion Lambda con el runtime Node.js 16.x y creado el rol de ejecucion "serverless-api-role"

![image](https://github.com/juan-conde-21/aws_lambda/assets/13276404/85ca2e20-ded3-4850-8441-0929bdbfcb74)

![image](https://github.com/juan-conde-21/aws_lambda/assets/13276404/2650bc6d-9d2c-423d-977b-48c6614f4fba)


3. Editar el rol creado para la funcion Lambda y agregar permisos para acceder a la tabla de DynamoDB (AmazonDynamoDBFullAccess y CloudWatchLogsFullAccess)

![image](https://github.com/juan-conde-21/aws_lambda/assets/13276404/0d3f4829-e6fd-466f-9896-1ee14e41318f)

![image](https://github.com/juan-conde-21/aws_lambda/assets/13276404/9e8c5058-19a9-4731-905b-3073501b3ead)

4. Crear el servicio API Gateway REST API "serverless-api"

![image](https://github.com/juan-conde-21/aws_lambda/assets/13276404/9422e612-9674-4c29-ad98-6014797a9561)

![image](https://github.com/juan-conde-21/aws_lambda/assets/13276404/a210cb33-dbfc-4533-9897-ed96b63d7813)

5. Crear los siguientes recursos y metodos:

  - health (GET)
  - product (DELETE, GET, PATCH, POST)
  - products (GET)
 
  ![image](https://github.com/juan-conde-21/aws_lambda/assets/13276404/14108357-c98d-49c3-a1b6-c29157117969)
  
  Agregar el metodo indicado en el punto anterior para cada recurso.
  
  ![image](https://github.com/juan-conde-21/aws_lambda/assets/13276404/178f7e86-06be-4eea-ba7b-6d4f77da8d61)
  
  Configuracion por metodo dependiendo el tipo.

  ![image](https://github.com/juan-conde-21/aws_lambda/assets/13276404/ad2c2441-b7a6-460d-8fdf-592e0e06957a)







