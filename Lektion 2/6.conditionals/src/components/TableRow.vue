<template>
  <tr>
    <th scope="row">{{ id }}</th>
    <td>{{ firstName }}</td>
    <td>{{ lastName }}</td>
    <td>{{ email }}</td>
  </tr>
</template>

<script>
export default {
    props: ['id', 'firstName', 'lastName', 'email']
};
</script>

<style>
</style>