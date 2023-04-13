# Desafio10

INTRUCCIONES PARA CORRER SERVICIOS:

1- Descargar librerias con comando: npm i  <br>
2- Correr servidor con comando: nodemon src/app.js <br> 

DESAFIO: <br>
1-Generar un módulo de Mocking para el servidor, con el fin de que, al inicializarse pueda generar y entregar 100 productos con el mismo formato que entregaría una petición de Mongo. Ésto solo debe ocurrir en un endpoint determinado (‘/mockingproducts’) <br>
2-Además, generar un customizador de errores y crear un diccionario para tus errores más comunes al crear un producto, agregarlo al carrito, etc. <br>

INSTRUCCIONES PARA REVISAR LO HECHO EN EL DESAFIO: <br>
1-Correr servicios (explicado en instrucciones para correr servicios) <br>
2-Utilizar postman para utilizar los endpoints del desafio <br>
3-Una vez en postman realizar una peticion GET con el siguiente endpoint: http://localhost:8080/mockingproducts 
(Deberia mostrar los 100 productos que creamos con la libreria @faker-js) <br>
4-Realizar una peticion POST con el siguiente endpoint: http://localhost:8080/api/products
agregando un body en formato raw (json) como el siguiente: <br>
{
    "title":"producto",
    "description":"descripcion de producto",
    "price":100,
    "code":"0x06e587",
    "quantity":4,
    "thumbnail":"Sin imagen",
    "category":"categoria"
} <br>
Al estar completo el objeto deberia realizar la peticion satisfactoriamente <br>
5-Realizar la misma peticion POST de productos nuevamente, pero 
en esta instancia agregar en el body un objeto donde falten agregar algunos de los
campos, como el siguiente objeto: <br>
{
    "description":"descripcion de producto",
    "price":100,
    "code":"0x06e587",
    "quantity":4,
    "thumbnail":"Sin imagen",
    "category":"categoria"
} <br>
Se deberia visualizar el custom error por la terminal diciendo que falta completar todos los campos
del producto.





