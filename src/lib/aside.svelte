<script>
 let username = "admin";
 let rol = "administrator";
 let showProfile = true;
 function togglemenu() {
     showProfile = !showProfile;
 }
</script>

<style>
 /* Styling for the hidden aside */
 .show-aside {
     top: 150px;
     float: left;
     padding: 10px;
     padding-bottom: 30%;
     background-color: #222;
     color: white;
     font-family: sans-serif;
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
{#if showProfile}
<button on:click={togglemenu}>-</button>
<aside class="show-aside">
    <p>Username: {username}</p>
    <p>User Role: {rol}</p>
</aside>
{:else}
<button on:click={togglemenu}>Menu</button>
{/if}
