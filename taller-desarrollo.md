# taller-desarrollo-notes
```bash
git config user.name "xlisden"
git config user.email "dayenira.delgado@gmail.com"
```
- Repositorio de archivos -> https://drive.google.com/drive/folders/1bMCGAqUW2qqACvsGOST2RzkqbqLXfvJD?usp=sharing

<details>
<summary><b>MongoDB</b></summary>

  - con comparaciones sql: https://learn.mongodb.com/learn/course/mongodb-sql-cheat-sheet/main/mongodb-sql-cheat-sheet
  - casi completo: https://www.geeksforgeeks.org/mongodb/mongodb-cheat-sheet/

</details>

<details>
<summary><b>17:12 30/09/2025</b></summary>
  
  - bus de eventos - a traves de el, se comunican los microservicios
  - se puede hacer un microservicio, que no este conectado a ninguna bd, pero si se encarga de orquestar a los microservicios, y no mezclarlos.
  - keycloak por si no se quiere implementar un microservicio de seguridad
  - **no existen claves foraneas**
  - por eso ya no se usan integers, si no UUID y GUID
  - para evitar la llamada a otro microservicios, se utiliza la replicacion de data
  - **patron saga** - ejecutar los pasos a la inversa, si en algun momento el algun microservicio se cae durante el evento
  - spring 3.5.6 - jdk 17
  - agregar swagger - url http://localhost:8080/swagger-ui/index.html
    ```
    <dependency>
    	<groupId>org.springdoc</groupId>
    	<artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
    	<version>2.5.0</version>
    </dependency>
    ```
  - 
  ---
  - que es escalar verticalmente? que es escalar horizontalmente?
  - que es gateway? - puerta de entrada para que le front, o un servicio externo, se comunique con el backend. No se hacen llamadas directamente al microservicio, se hace a traves del API gateway, porque ahi estan la seguridad
  - config server? - medida de seguridad adicional para proteger los datos sensibles
  - seq: https://dev.to/minhaz1217/java-spring-boot-use-seq-for-logging-39fm
     --https://github.com/minhaz1217/java-quarkus/tree/master/spring-boot-seq

</details>

<details>
<summary><b>17:05 7/10/2025</b></summary>
  
  - google drive tiene versionamiento
  - hot fix: cambio en produccion
  - cherry-pick: pasar solo un commit a una rama, no todos los cambios completos

</details>


<details>
<summary><b>17:10 21/10/2025</b></summary>
  
  - contenedores != a maquinas virtuales
    - mv - ocupa espacio: 32GB de RAM se puede crear 3maq de 8GB, para yo quedarme con 8
    - con - designa los recursos necesarios (espacio de memoria) para funcionar. No se necesita levantanr un SO para que funcione. Reutiliza componetnes del SO anfitrion
  - registry = nube. donde estan las imagenes
  - cliente: terminal o docker desktop
  - contendor != imagen
  - build, pull, run
  - imagnees = plantilla de sola lectura. a partir de umna sola imagebn. se crean N contenedores
  - descargar composes
    ```bash
    docker compose -f compose-database-mysql.yml up -d
    ```
  - public key not allowed
    1. driver properties
    2. allow public key retrival cambiar a true
  - usar db en postregres
    ```sql
    SET search_path TO base_de_datos;
    ```
  - mongo
    - collecion == tabla
</details>

<details>
<summary><b>16:27 28/10/2025</b></summary>

  1. implementar las databases con las versiones latest (se actualizo docker en el repositorio)
  2. 4 microservicios y un gateway

  - siempre se debe implementar un log de errores

  **Buenas practicas**
  - validaciones - con manejo de excepciones (se maneja mejor con centralizacion de excepcioens) - GlobalExceptionHandler
    -  al implementar throws exception, no se necesita el try catch
  - los logs tambien son informativos o de advertencia, no solo de errores
    
</details>

<details>
<summary><b>18:00 2/12/2025</b></summary>
  
  - configurar logica de deasctivacion
  - traer todos los items activos
  - verificar existencias entre archivos activos
  - clase abstracta para los campos de auditoria
  - analizar relaciones con las nuevas tablas
  - implementar cuantas escuelas hay por facultad
  - analizar nuevos endpoints resultantes de las tablas

</details>

<hr/>
<details>
<summary><b>plantilla</b></summary>
  
  - item

</details>
