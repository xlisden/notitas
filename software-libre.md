# soft-libre-notes
```bash
git config user.name "xlisden"
git config user.email "dayenira.delgado@gmail.com"
```
```bash
npm i express cors dotenv mysql2
npm i --save-dev nodemon
```
- [Angular notes](https://app.capacities.io/home/2f182914-42b1-40b3-94c9-50b702c65c46)
- [Nodejs best practices](https://github.com/goldbergyoni/nodebestpractices/blob/spanish-translation/README.spanish.md)
- [Git/GitHub](https://xlisden.notion.site/Git-GitHub-4da26f209cc040b3a72ae09038c11bf3)

- auto close tag - jun han
- auto import - steoates
- auto rename tag - jun han
- prettier eslint - rebecca vest

---
### 19:46 26/09/2025
- node js v22 - 22.20.0
- angular v19 
  ```
  npm install -g @angular/cli@19.2.0
  ```
- permitir los scripts: 
  Powershell en modo admin
  ```
  Set-ExecutionPolicy Unrestricted
  ```
- desinstalar Angular
  ```
  npm uninstall -g @angular/cli
  ```
- generar componente
  ```
  ng g c carpeta/componente --change-detection Default --inline-style --skip-tests
  ```
### 17:36 1/10/2025
- paquetes para variables de entorno, mysql, express framework 5.1.0, el cors para comunicarnos con el front seguramente, monitor de cambios el nodemon
  ```
  npm i express cors
  npm i mysql2 dotenv cors
  npm i --save-dev nodemon
  ```
- bd bibliotecadb
  ```
  CREATE SCHEMA IF NOT EXISTS bibliotecadb
  CREATE TABLE `bibliotecadb`.`libros` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `titulo` VARCHAR(45) NULL,
    `autor` VARCHAR(45) NULL,
    `isbn` VARCHAR(45) NULL,
    `editorial` VARCHAR(45) NULL,
  PRIMARY KEY (`id`));
  ```
- los envs van al mismo nivel del package json o en root
