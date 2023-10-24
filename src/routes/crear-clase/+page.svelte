<body>
    <div class="titulo-registro-clases">
        <p>Registro clases | Crear Clase</p>
    </div>
    <main>
        <h2 class="subtitulo-registro">Nueva Clase</h2>
        <div class="Especialidad">
            <label for="especialidad">Especialidad</label>
            <br>
            <select name="especialidad" id="especialidad">
            <option value="computacion">Computación</option>
            <option value="construcciones">Construcciones</option>
            <option value="quimica">Quimica</option>
            <option value="electronica">Electronica</option>
            <option value="electrica">Electrica</option>
            <option value="mecanica">Mecanica</option>
            </select>
        </div>

        <!--falta agregar todas las materias por el backend-->
        <div class="Materia">
            <label for="materia">Materia</label>
            <br>
            <select name="materia" id="materia">
            <option value="practicas-profesionalizantes">Practicas Profesionalizantes</option>
            </select>
        </div>
        
        <div class="horarios">
            <!--Falta agregar los horarios-->
        </div>

        <div class="profesores">
            <label for="profesores">Profesores</label>
            <input type="text" id="profesores" name="profesores">
        </div>

        <div class="identf-clase">
            <div class="anio">
                <label for="anio">Año</label>
                <br>
                <select name="anio" id="anio">
                <option value="sexto">6</option>
                <option value="quinto">5</option>
                </select>
            </div>
            <div class="division">
                <label for="division">división</label>
                <br>
                <select name="division" id="division">
                <option value="primero">1</option>
                <option value="segundo">2</option>
                </select>
            </div>
            <div class="turno">
                <label for="turno">Turno</label>
                <br>
                <select name="turno" id="turno">
                <option value="tarde">tarde</option>
                <option value="mañana">mañana</option>
                </select>
            </div>
        </div>
    </main>

    <div class="crear-clase-button">
        <button type="button">Crear Clase</button>
    </div>
</body>