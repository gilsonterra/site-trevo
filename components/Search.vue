<template>
  <div class="search-container">
    <input
      type="search"
      class="search-input"
      placeholder="Encontre os melhores laboratórios, médicos e clínicas"
    />
    <button class="search-button">Buscar</button>
  </div>
</template>

<style scoped>
.search-container {
  padding: 5px;
  display: flex;
  justify-content: start;
  align-items: center;
  gap: 5px;
}

.search-input {
  height: 3rem;
  flex: 1;
  border: none;
  background: #eee;
  padding: 10px;
}

.search-button {
  height: 3rem;
  width: 100px;
  background-color: #695673;
  color: white;
  border: none;
  border-radius: 5px;
  font-size: 1rem;
  cursor: pointer;
}

.search-button:hover {
  background-color: #5d4a64;
}
</style>
