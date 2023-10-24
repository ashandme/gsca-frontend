<body>
    <main>
        <h2>Configuración / Privilegios</h2>

        <a href="">Profesor</a>
        <form action="adminyprof">
            <label for="adminyprof">Administrador y profesor</label>
            <input type="checkbox" name="Nombre" id="nombre"> Nombre
            <input type="checkbox" name="Apellido" id="apellido"> Apellido
            <input type="checkbox" name="Telefono" id="telefono"> Telefono
            <input type="checkbox" name="dni" id="dni"> DNI
            <input type="checkbox" name="gmail" id="gmail"> Gmail

            <label for="alumno">Alumno</label>
            <input type="checkbox" name="Nombre" id="nombre"> Nombre
            <input type="checkbox" name="Apellido" id="apellido"> Apellido
            <input type="checkbox" name="dni" id="dni"> DNI
            <input type="checkbox" name="Fecha Nacimiento" id="fecha-nacimiento"> Fecha de Nacimiento
            <input type="checkbox" name="ID" id="id"> ID
            <input type="checkbox" name="Gmail" id="gmail"> Gmail
            <input type="checkbox" name="Telefono" id="telefono"> Telefono

            <p>Datos que el profesor puede ver de cada usuario</p>

        </form>
            
         <a href="">Administrador</a>
         
         <form action="registrar-alumno">
            <input type="checkbox" name="Nombre" id="nombre"> Registrar alumno
            <label for="cant-min">Cantidad minima</label>
            <input type="number" name="cant-min" id="cant-min">
            <label for="cant-min">Cantidad maxima</label>
            <input type="number" name="cant-max" id="cant-max">
         </form>
         <input type="checkbox" name="registrar-usuarios" id="registrar-usuarios">Registrar Usuarios
         <form action="registrar-usuario">
            <input type="checkbox" name="registrar-administradores" id="registrar-administradores"> Registrar Administradores
            <input type="checkbox" name="crear-otros-administradores" id="crear-otros-administradores"> Pueden crear otros Administradores
            <input type="checkbox" name="registrar profesores" id="registrar-profesores"> Registrar Profesores
         </form>
         

    </main>
    <button>Guardar Cambios</button>
</body>