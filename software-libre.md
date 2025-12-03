# soft-libre-notes
```bash
git config user.name "xlisden"
git config user.email "dayenira.delgado@gmail.com"
```
<details>
<summary><b>ExpressJs</b></summary>
  
  - dependencias
      ```bash
      npm i express cors dotenv mysql2
      npm i --save-dev nodemon
      ```
  - iniciar
      ```bash
      npm init -y
      ```
  - run
      ```bash
      node index.js
      ```

</details>

<details>
<summary><b>Angular / Tailwind / DaisyUI</b></summary>
  
  - https://daisyui.com/docs/install/angular/
  ```bash
  npm install daisyui@latest tailwindcss@latest @tailwindcss/postcss@latest postcss@latest --force
  ```

  - crear archivos
  ```bash
  ng g s nombreServicio --skip-tests
  ```

</details>

<details>
<summary><b>Otros</b></summary>

  - [Angular notes](https://app.capacities.io/home/2f182914-42b1-40b3-94c9-50b702c65c46)
  - [Nodejs best practices](https://github.com/goldbergyoni/nodebestpractices/blob/spanish-translation/README.spanish.md)
  - [Git/GitHub](https://xlisden.notion.site/Git-GitHub-4da26f209cc040b3a72ae09038c11bf3)

- auto close tag - jun han
- auto import - steoates
- auto rename tag - jun han
- prettier eslint - rebecca vest
</details>

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
  ```sql
  CREATE SCHEMA IF NOT EXISTS bibliotecadb;
  USE `bibliotecadb`;
  
  CREATE TABLE `bibliotecadb`.`libros` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `titulo` VARCHAR(45) NULL,
    `autor` VARCHAR(45) NULL,
    `isbn` VARCHAR(45) NULL,
    `editorial` VARCHAR(45) NULL,
  PRIMARY KEY (`id`));
  ```
- los envs van al mismo nivel del package json o en root

### 17:39 15/10/2025
- insertar libros
    ```sql
    INSERT INTO `bibliotecadb`.`libros`
    (`id`, `titulo`, `autor`, `isbn`, `editorial`)
    VALUES
    (1, 'Cien años de soledad', 'Gabriel García Márquez', '978-3-16-148410-0', 'Editorial Sudamericana'),
    (2, 'Don Quijote de la Mancha', 'Miguel de Cervantes', '978-84-376-0494-7', 'Editorial Planeta'),
    (3, 'La sombra del viento', 'Carlos Ruiz Zafón', '978-84-08-05306-6', 'Editorial Planeta'),
    (4, 'Ficciones', 'Jorge Luis Borges', '978-84-95060-01-7', 'Editorial Alianza'),
    (5, 'El amor en los tiempos del cólera', 'Gabriel García Márquez', '978-84-376-3433-3', 'Editorial Oveja Negra'),
    (6, 'Los detectives salvajes', 'Roberto Bolaño', '978-84-339-4249-0', 'Editorial Anagrama');
    ```
- categoria
  ```sql
  CREATE TABLE IF NOT EXISTS `bibliotecadb`.`categoria` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `nombre` VARCHAR(45) NULL,
  PRIMARY KEY (`id`));
  
  ALTER TABLE `bibliotecadb`.`libros` 
  ADD COLUMN `categoria_id` INT NULL AFTER `editorial`;
  
  ALTER TABLE `bibliotecadb`.`libros` 
  ADD CONSTRAINT fk_libros_categoria
  FOREIGN KEY (categoria_id)
  REFERENCES categoria(id)
  ON DELETE SET NULL;

  INSERT INTO `bibliotecadb`.`categoria`
  (`nombre`)
  VALUES
  ( 'drama'), ( 'comedia'), ( 'biografia');
  
  
  UPDATE libros SET categoria_id = 3 WHERE id = 1;
  
  SELECT * FROM libros WHERE categoria_id = 3;
  
  SELECT * FROM categoria ORDER BY id DESC;
  
  SELECT * FROM libros;
  
  ```
- autor
  ```sql
  CREATE TABLE IF NOT EXISTS `bibliotecadb`.`autor` (
  `id` INT NOT NULL AUTO_INCREMENT,
  `nombre` VARCHAR(100) NULL,
  PRIMARY KEY (`id`)
  );
  ALTER TABLE `bibliotecadb`.`libros`
  ADD COLUMN `autor_id` INT NULL AFTER `categoria_id`;
  ALTER TABLE `bibliotecadb`.`libros`
  ADD CONSTRAINT fk_libros_autor
  FOREIGN KEY (autor_id)
  REFERENCES autor(id)
  ON DELETE SET NULL;
  INSERT INTO `bibliotecadb`.`autor` (`nombre`) VALUES
  ('Gabriel García Márquez'),
  ('Miguel de Cervantes'),
  ('Carlos Ruiz Zafón'),
  ('Jorge Luis Borges'),
  ('Roberto Bolaño');
  ```  
---


