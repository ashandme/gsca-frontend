<script>
 let username = "Nombre Apellido";
 let rol = "Administrador";
 let showProfile = true;

 function togglemenu() {
    let aside = document.getElementById('aside');
     showProfile = !showProfile;
     console.log("hizo click");
     if (!showProfile) {
        console.log("es verdadera");
        aside.style.opacity = '0'; // Hace que el aside sea invisible gradualmente
        aside.style.transition = 'opacity 10s'; // Agrega una transición de 0.5 segundos
    } else {
        console.log("es falsa");
        aside.style.opacity = '1'; // Restaura la opacidad original
    }
 }
</script>


{#if showProfile}
<button on:click={togglemenu}>-</button>
<aside class="show-aside" id="aside"> 
    <div class="perfil-frontal">
        <div class="perfil"></div>
        <div class="perfil-frontal-datos">
            <p class="username">{username}</p>
            <p class="rol">{rol}</p>
        </div>
    </div>
    <div class="opciones">
        <div class="componente">
            <a href="#">Registro Clases</a>
        </div>
        <div class="componente ">
            <a href="#">Registro Usuarios</a>
        </div>
        <div class="componente">
            <a href="#">Configuración</a>
        </div>
    </div>
    
</aside>
{:else}

<aside class="show-aside" id="aside" style="opacity: 0;">
    <div class="perfil-frontal">
        <div class="perfil"></div>
        <div class="perfil-frontal-datos">
            <p class="username">{username}</p>
            <p class="rol">{rol}</p>
        </div>
    </div>
    <div class="opciones">
        <div class="componente">
            <a href="#">Registro Clases</a>
        </div>
        <div class="componente ">
            <a href="#">Registro Usuarios</a>
        </div>
        <div class="componente">
            <a href="#">Configuración</a>
        </div>
    </div>
    
</aside>
<button class="boton" on:click={togglemenu}>Menu</button>
    
{/if}


<style>
 /* Styling for the hidden aside */
 *{
    margin: 0px;
    padding: 0px;
    font-family: 'Roboto';
 }

 

 .show-aside {
     top: 150px;
     float: left;
     /*padding: 10px;*/
     padding-bottom: 50%;
     background-color: #222;
     color: white;
     width: 262px;
     transition: background-color .10s;
 }

.perfil-frontal{
    display: flex;
    flex-direction: row;
    align-items: center;
    margin: 10px;
}
 .show-aside .perfil{
    background-color:#E7E6E6;
    border-radius: 100%;
    width: 80px;
    height: 80px;
    /*display: inline-block;*/
}
.perfil-frontal-datos{
    /*display: inline-block;*/
    margin-left: 34px;
}
.show-aside .username{
    margin: 0px;
}
 .show-aside .rol{
    font-size: 13px;
    margin: 0px;
}

.componente a{
    text-decoration: none;
    color: rgb(255, 255, 255);
    display: flex;
    justify-content: center;
    padding: 8.3% 0%;
    align-items: center;
    transition: background-color 0.7s;
    
}

a:hover{
    background-color: #767171;
}


 /* Styling for the button */
 button {
     background-color: #a70900;
     color: white;
     padding: 5px 10px;
     border: none;
     cursor: pointer;
 }
</style>


