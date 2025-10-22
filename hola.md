- db
```javascript
const mysql = require('mysql2');

const pool = mysql.createPool({
  host: 'localhost',
  user: 'root',
  database: 'dssl-para-practica-01',
  password: '123456',
  waitForConnections: true,
  connectionLimit: 10,
  queueLimit: 0
});

const promisePool = pool.promise();

pool.getConnection((err, connection) => {
  if (err) {
    console.log(`error`);
  } else {
    console.log(`listo`);
    connection.release();
  }
});

module.exports = promisePool;
```
- index
```javascript
const express = require('express');
const cors = require('cors');

const discosRoutes = require('./routes/discosRoutes');
const cancionesRoutes = require('./routes/cancionesRoutes');

const app = express();
const PORT = 3000;

app.use(cors());
app.use(express.json());
app.use(express.urlencoded({ extended: true }));

app.use('/api/discos', discosRoutes);
app.use('/api/canciones', cancionesRoutes);

app.get('/', (req, res) => {
    res.json({
        mensaje:"API-Para-practica01"
    });
});

app.listen(PORT, () => {
    console.log(`http://localhost:${PORT}`);    
});
```

- controller
```javascript
async function name(req, res) {
  try {

    res.status(200).json({
      sucess: true,
      count: objeto.length,
      data: objeto
    });
  } catch (error) {
    const statusCode = error.status || 500;
    res.status(statusCode).json({
      sucess: false,
      mensaje: "Error en name()",
      data: error.message
    });
    console.log(`name()-discos => ${error}`);
  }
}
```
