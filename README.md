# LENGUAJE-PHP

<br>
PARECE SENCILLO PERO SE DEBE DE TENER EN CUENTA VARIAS COSAS AL MOMENTO DE TENER UNA CONEXION PHP CON LA BASE DE DATOS Y EL SERVIDOR DONDE ESTEN ALOJADOS Y PODER TENER UN BUEN FUNCIONAMIENTO ESTE ES UN CODIGO QUE CONECTA CON LA BASE DE DATOS TAMBIEN USA UN LENGUAJE MYSQL
<br>
<pre>
      
    <?php
$servername = "localhost";
$username = "root";
$password = "";

// Conexión sin especificar la base de datos
$conn = new mysqli($servername, $username, $password);

// Verificar conexión
if ($conn->connect_error) {
    die("CONEXION FALLIDA: " . $conn->connect_error);
}

// Consulta para crear la base de datos
$sql = "CREATE DATABASE IF NOT EXISTS Alumnos";

if ($conn->query($sql) === TRUE) {
    echo "BASE DE DATOS CREADA CORRECTAMENTE";
} else {
    echo "ERROR AL CREAR LA BASE DE DATOS: " . $conn->error;
}

// Cerrar conexión
$conn->close();
?>
    </pre>
</body>
</html>


// Cerrar conexión
$conn->close();
?>
</pre>
