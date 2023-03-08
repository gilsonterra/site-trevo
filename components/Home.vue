<template>
  <div class="layout">
    <Header />
    <Search />
    <main class="main">
      <Sidebar />
      <Main />
    </main>
  </div>
</template>

<style scoped>
.layout {
  display: grid;
  grid-template-rows: auto 80px 1fr;
}

.main {
  display: grid;
  gap: 30px;
  grid-template-columns: 300px 1fr;
}
</style>
