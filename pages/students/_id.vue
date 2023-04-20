<template>
  <div class="student_id">
    <h2>{{ studentName }}</h2>
    <p>
      <NuxtLink to="/students">生徒一覧へ戻る</NuxtLink>
      <span>｜</span>
      <NuxtLink to="/">トップページへ</NuxtLink>
    </p>
  </div>
</template>

<script>
export default {
  validate({ params }) {
    const id = params.id;
    const validIds = [
      "qnfungqxllc3m1ak",
      "7j9cumkgsq6l264c",
      "eo34bhey9m0d92ou",
    ];
    return validIds.includes(id);
  },
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
  computed: {
    studentName() {
      const studentId = this.$route.params.id;
      const student = this.students.find(function (students) {
        return students.id === studentId;
      });
      return student ? student.name : "";
    },
  },
};
</script>

<style>
h2 {
  margin: 2px;
}

p {
  margin: 2px;
}

.student_id {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
