<template>
  <div class="container">
    <table>
      <tr>
        <th><h2>生徒一覧</h2></th>
        <th><h2>管理者</h2></th>
      </tr>
      <tr>
        <td><NuxtLink to="/students">生徒の情報を見る</NuxtLink></td>
        <td><NuxtLink to="/management">管理画面を見る</NuxtLink></td>
      </tr>
    </table>
  </div>
</template>

<style>
th,
td {
  height: 30px;
  width: 160px;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
