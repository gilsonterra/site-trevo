<template>
  <aside class="aside">
    <ul>
      <li><h2>Localização</h2></li>
      <li><a href="#">Até 1km</a></li>
      <li><a href="#">de 1km até 5km</a></li>
      <li><a href="#">Mais 5km</a></li>
      <li><h2>Laboratórios</h2></li>
      <li><a href="#">Matriz</a></li>
      <li><a href="#">Entre 2 e 3</a></li>
    </ul>
  </aside>
</template>

<style scoped>
.aside {
  padding: 5px;
}

.aside h2 {
  padding: 5px;
  margin: 0px;
  font-size: 1rem;
  background: #eee;
  color: #695673;
}

.aside ul {
  list-style-type: none;
  padding: 0px;
  margin: 0px;
}

.aside ul li {
  padding: 10px;
  color: #4d4d4d;
  font-size: 0.9rem;
}

.aside ul li a {
  text-decoration: none;
  color: #695673;
}

.aside ul li a:hover {
  text-decoration: underline;
}
</style>
