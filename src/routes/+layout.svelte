<script>
 import Nav from "$lib/nav.svelte";
 import Aside from "$lib/aside.svelte";
</script>

<body>
    <Nav />
    <Aside />
</body>

<slot></slot>

<style>
 body {
     margin: 0;
 }
</style>
