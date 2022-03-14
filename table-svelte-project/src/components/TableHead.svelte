<script>
export let headerArray = []

</script>

<tr class="headers">
    {#each headerArray as header, i}
    <th>{header}</th>
    {/each}
</tr>