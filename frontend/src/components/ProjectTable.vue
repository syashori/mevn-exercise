<template>
  <h1 class="display-2 font-weight-bold mb-3">
     Project Management Page
  </h1>
  <v-table>
    <thead>
      <tr>
        <th class="text-left">
          Title
        </th>
        <th class="text-left">
          image
        </th>
        <th class="text-left">
          description
        </th>
        <th class="text-left">
          action
        </th>
      </tr>
    </thead>
    <tbody>
      <tr
        v-for="item in desserts"
        :key="item.name"
      >
        <td>{{ item.name }}</td>
        <td>{{ item.calories }}</td>
        <td>{{ item.description }}</td>
        <td>action</td>
      </tr>
    </tbody>
  </v-table>
</template>
<script>
  export default {
    data () {
      return {
        desserts: [
          {
            name: 'Frozen Yogurt',
            calories: 159,
            description: "description 1",
          },
          {
            name: 'Frozen Yogurt',
            calories: 159,
            description: "description 1",
          },
        ],
      }
    },
  }
</script>