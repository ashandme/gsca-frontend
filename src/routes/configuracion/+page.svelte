<body>
        <center><h2>Configuración</h2></center>
        <h3>Perfil</h3>
    <main>
        <div class="caja2">
                <div class="caja">
                        <label for="nombre">Nombre/s</label><br>
                        <input type="text" id="nombre-usuario" name="nombre">
                    </div>   
                    <div class="caja">
                        <label for="telefono">Telefono</label><br>
                        <input type="number" id="telefono" name="telefono">
                    </div>
        </div>
        
        <div class="caja2">                
            <div class="caja">
                    <label for="dni">DNI</label><br>
                    <input type="number" id="dni" name="dni">
            </div>

            <div class="caja">
                <label for="gmail">Gmail</label><br>
                <input type="mail" id="gmail" name="gmail">
            </div>
        </div>
            
    </main>
            
    <button onclick="guardarCambios()" class="boton-guardado">Guardar</button>

    <a href="./configuracion/cambio-contrasenia"><img src="img1.png" alt="cambiar-contraseña"></a>
    <a href="./configuracion/privilegios"><img src="img2.png" alt="privilegios"></a>
    <a href="./configuracion/asistencia"><img src="img3.png" alt="asistencia"></a>
    <a href="/"><img src="img4.png" alt="manual-de-usuario"></a>
</body>
<style>
    *{
    margin: 0;
    padding: 0;
    font-family: sans-serif;
}
main{
    width: 1000px;
    background-color: green;
    display: table-cell;
    left: 50%;
    margin-left: auto;

}
.caja{
    /*display: table-cell;*/
    display: inline-block;
}
.caja2{
    /*display: grid;*/
    padding-left: 10%;
    background-color: blue;
    /*argin: auto;*/
    margin: 10% 0%;
    color: white;
}
.boton-guardado{
    width: 7%;
    font-size: 100%;
    border-radius: 5px;
    background-color: rgb(192,0,0);
    padding: 10px;
    font-style: initial;
    float: right;
    color: white;
}
input{
    width: 270px;
}
</style>