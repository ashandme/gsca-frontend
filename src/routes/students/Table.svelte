<script>
 import { studentData } from '../data.js';
 const tableHeaders = ["Id", "Surname", "Name", "DNI"];
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
    {#each studentData as item}
      <tr>
        <td>{item.id}</td>
        <td>{item.surname}</td>
        <td>{item.name}</td>
        <td>{item.dni}</td>
      </tr>
    {/each}
  </tbody>
</table>
