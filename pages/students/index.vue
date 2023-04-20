<template>
  <div class="students">
    <h2>生徒一覧</h2>
    <ul>
      <li v-for="student in students" v-bind:key="student.id">
        <NuxtLink :to="{ path: `/students/${student.id}` }">{{student.name}}</NuxtLink>
      </li>
    </ul>
    <NuxtLink to="/">戻る</NuxtLink>
  </div>
</template>

<script>
export default {
  data() {
    return {
      students: [
        {
          id: "qnfungqxllc3m1ak",
          name: "生徒A",
        },
        {
          id: "7j9cumkgsq6l264c",
          name: "生徒B",
        },
        {
          id: "eo34bhey9m0d92ou",
          name: "生徒C",
        },
      ],
    };
  },
};
</script>

<style>
.students {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.students h2 {
  display: block;
}
</style>
