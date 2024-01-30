<script>
    import svelteTable from "svelte-table"
    import {faker} from "@faker-js/faker"
    faker.seed(5);


    let sortBy = "id";
    let iconAsc = "↑";
    let iconDesc = "↓";
    let selectedCols = ["id", "first_name", "last_name"];
    let numRows = 10;
    let data = [];


    let generateData = () => {
    data = Array(numRows)
      .fill("")
      .map((n, i) => {
        let d = {
          id: i,
          first_name: faker.person.firstName(),
          last_name: faker.person.lastName()
        };
        return d;
      });
  };


</script>