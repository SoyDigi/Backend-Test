# Challenge Backend - Python 🐍

**Tu tarea:** 
El desafío consiste en desarrollar una API para explorar los distintos servicios que ofrecen nuestros Freelancers y como están conformados cada uno de ellos. 

El entregable de la prueba será el código que has desarrollado un proyecto que podamos levantar en un docker.  

Tu aplicación nos debe permitir: 

- Visualizar todos los servicios 

- Seleccionar un servicio 

- Visualizar los entregables asociados al servicio seleccionado 

Sorpréndenos con tus capacidades, no se trata solo de terminar una prueba, se trata de mostrar tu pasión por el desarrollo, la resolución de problemas, el código limpio y claro y el interés que le pones a las cosas. Cualquiera puede codificar, pero no todos lo hacen con verdadero orgullo. 

**Criterios por evaluar:**

A la hora de evaluar tu prueba técnica, tendremos en cuenta lo siguiente: 

- Organización del código: la estructura del proyecto debe ser limpia y ordenada.  
- Claridad: El proyecto debe poder ejecutarse de forma sencilla siguiendo un readme, que contenga las instrucciones para: utilizarse creando un entorno virtual(venv), instalar las dependencias necesarias con pip, configurar la conexión a la base de datos. 
- Asertividad: ¿Toda la aplicación está funcionando? Si falta algo, ¿el README explica por qué?. 
- Legibilidad del código (incluidos los comentarios). 
- Cobertura: Deberá tener Unit Test implementado con una cobertura del 80% mínimo.  
- La prueba será conectada a nuestro Front y debe funcionar perfectamente.  

**Requerimientos técnicos** 

Tu proyecto deberá cumplir con los siguientes requerimientos: 

**1) Creación de tablas en la Base de datos**

La base de datos debe cumplir con los siguientes requisitos: 

- La base de datos debe ser PostgreSQL. 

- Los datos de la conexión deben poder configurarse fácilmente para facilitar el deploy en un nuevo ambiente de ser necesario.  

**Modelado de la base de datos**

La base de datos debe de tener 2 tablas que consistirán en lo siguiente: 

**Tipos de servicios:**

- ID 

- Nombre 

**Paquete:**

- Descripción 

- Precio 

- Entregables 

- Entregable ID 

- Tipos de servicios ID 

**IMPORTANTE:**
Las dos tablas se relacionan por el ID del tipo de servicio en una relación de uno a muchos.  

**2) Rutas:**

**GET /services:**

Endpoint con el cual podemos obtener el listado de los tipos de Servicios.
La ruta debera tener la siguiente estructura:
[
    {
        "id": 1,
        "name": "Desarrollos On-Cloud",
        "packages": [
            {
                "id": 1,
                "description": "Lorem ipsum dolor sit amet, consectetur adipiscing eli",
                "price": 100,
                typeOfServiceID: 1,
                "deliverables": [
                    {
                        "id": 1,
                        "name": "Include source code",
                        "description": null,
                        "included": false,
                        "amount": 0,
                        "enabled": true
                    }
                ]
            }
        ]   
     }
  ]

**GET /services/{id}:**

Endpoint que recibe el tipo de servicio y devuelve los paquetes con sus respectivos entregables. 
La ruta debera tener la siguiente estructura: 
    {
        "id": 1,
        "name": "Desarrollos On-Cloud",
        "packages": [
            {
                "id": 1,
                "description": "Lorem ipsum dolor sit amet, consectetur adipiscing eli",
                "price": 100,
                typeOfServiceID: 1,
                "deliverables": [
                    {
                        "id": 1,
                        "name": "Include source code",
                        "description": null,
                        "included": false,
                        "amount": 0,
                        "enabled": true
                    }
                ]
            }
        ]   
     }

**3) Testing:**
Deberá tener Unit Test implementado con una cobertura del 80% mínimo. 

**Documentación:**
Documentar los endpoints utilizando Postman o Swagger. 

**Al finalizar la prueba:**
Deberás enviar la solución asociada a un repositorio de GitHub, el cual debe de ser publico, debes compartirlo con la persona que revisará tu solución (usuario: 
laurawarjan) y por ultimo compartir el enlace de la misma con nosostros.
