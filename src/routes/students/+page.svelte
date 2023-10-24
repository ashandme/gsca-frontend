<script>
    let studentData = {
        id: null,
        id_fingerprint: null,
        dni: null,
        name: '',
        surname: ''
    };
    import Table from './Table.svelte'; // Import the Svelte component
    async function handleSubmit() {
    const url = 'http://localhost:3000/student';

    try {
      const response = await fetch(url, {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json'
        },
        body: JSON.stringify(studentData)
      });

      if (response.ok) {
        console.log('Estudiante creado exitosamente');
        location.reload();
      } else {
        console.error('Error al crear el estudiante');
      }
    } catch (error) {
      console.error('Error:', error);
    }
  }
</script>
<style>
  article {
      margin: 10px;
      font-family: Arial, Helvetica, sans-serif;
  }
</style>
<article>
    <h1>Estudiantes</h1>
    <form on:submit|preventDefault="{handleSubmit}">
    <label>
    DNI:
    <input type="number" bind:value="{studentData.dni}" />
    </label>
    <br />
    <label>
    Nombre:
    <input type="text" bind:value="{studentData.name}" />
    </label>
    <br />
    <label>
    Apellido:
    <input type="text" bind:value="{studentData.surname}" />
    </label>
    <br />
    <button type="submit">Guardar</button>
    </form>
    <Table />
</article>
