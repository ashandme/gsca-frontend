<script>
  import { onMount } from 'svelte';
  let studentData;

  onMount(async () => {
    const url = 'http://localhost:3000/students';

    try {
      const response = await fetch(url);
      const data = await response.json();
      studentData = data;
    } catch (error) {
      console.error('Error:', error);
    }
  });
 const tableHeaders = ["Id", "FID" ,"Surname", "Name", "DNI"];
</script>

<style>
 .students {
     font-family: Arial, Helvetica, sans-serif;
     border-collapse: collapse;
     width: 50%;
 }
 .students th {
  padding-top: 12px;
  padding-bottom: 12px;
  text-align: left;
  background-color: #a70A00;
  color: white;
 }
 .students tr:nth-child(even){
     background-color: #f2f2f2;
 }
</style>

<table class="students">
  <thead>
    <tr>
      {#each tableHeaders as header}
        <th>{header}</th>
      {/each}
    </tr>
  </thead>
  <tbody>
  {#if studentData}
    {#each studentData as item}
      <tr>
        <td>{item.id}</td>
        <td>{item.id_fingerprint}</td>
        <td>{item.surname}</td>
        <td>{item.name}</td>
        <td>{item.dni}</td>
      </tr>
    {/each}
  {:else}
  <p>No hay datos disponibles</p>
  {/if}
  </tbody>
</table>
