<script>
 import Nav from "$lib/nav.svelte";
 import Aside from "$lib/aside.svelte";
</script>

<body>
    <Nav />
    <Aside />
    <slot />
</body>


<style>
 body {
     margin: 0;
 }
</style>
