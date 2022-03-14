<script>
import faker from "@faker-js/faker";
import TableHead from "./TableHead.svelte";
import TableRow from "./TableRow.svelte";


let people = [];


for (let i = 0; i < 50; i++) {
    const person = {
        name: faker.name.findName(),
        avatar: faker.image.avatar(),
        city: faker.address.city()
    }
    people.push(person);
}
let headerArray = Object.keys(people[0])


</script>

<table>
    <TableHead headerArray = {headerArray}/>
    <TableRow objectArray = {people} headerArray = {headerArray}/>
</table>