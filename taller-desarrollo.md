# taller-desarrollo-notes
```bash
git config user.name "xlisden"
git config user.email "dayenira.delgado@gmail.com"
```
### 17:12 30/09/2025
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

### 17:05 7/10/2025

- google drive tiene versionamiento
- hot fix: cambio en produccion
- cherry-pick: pasar solo un commit a una rama, no todos los cambios completos

<details>
<summary><b>17:10 21/10/2025</b></summary>
  
  - contenedores != a maquinas virtuales
    - mv - ocupa espacio: 32GB de RAM se puede crear 3maq de 8GB, para yo quedarme con 8
    - con - designa los recursos necesarios (espacio de memoria) para funcionar. No se necesita levantanr un SO para que funcione. Reutiliza componetnes del SO anfitrion

</details>
