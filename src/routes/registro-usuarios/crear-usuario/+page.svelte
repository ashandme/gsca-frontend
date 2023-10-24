<body>
    <div class="titulo-registro-usuarios">
        <p>Registro Usuarios | Crear Usuario</p>
    </div>
    <main>
        <h2 class="subtitulo-registro">Nueva Usuario</h2>
      
        <div class="rol">
            <label for="rol">Rol</label>
            <br>
            <select name="rol" id="rol">
            <option value="administrador">Administrador</option>
            <option value="profesor">Profesor</option>
            </select>
        </div>

        <!--falta agregar todas las materias por el backend-->
        <div class="nombre">
            <label for="nombre">Nombre/s</label>
            <input type="text" id="nombre-usuario" name="nombre">
        </div>
        
        <div class="apellido">
            <label for="apellido">Apellido/s</label>
            <input type="text" id="apellido-usuario" name="apellido">
        </div>

        <div class="dni">
            <label for="dni">DNI</label>
            <input type="number" id="dni" name="dni">
        </div>

        <div class="telefono">
            <label for="telefono">Telefono</label>
            <input type="number" id="telefono" name="telefono">
        </div>

        <div class="gmail">
            <label for="gmail">Gmail</label>
            <input type="mail" id="gmail" name="gmail">
        </div>

        <div class="contrasenia">
            <label for="contrasenia">Contraseña</label>
            <input type="password" id="contrasenia" name="contrasenia">
        </div>

        <div class="agregar-huella">
            <!--falta agregar la funcionalidad-->
        </div>
    </main>
    <div class="crear-clase-button">
        <button type="button">Crear Usuario</button>
    </div>
</body>