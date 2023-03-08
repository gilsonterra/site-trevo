<template>
  <header class="header">
    <div class="img-container">
      <img
        height="35em"
        src="data:image/png;base64,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"
        alt="trevo"
      />
    </div>

    <nav class="nav">
      <ul>
        <li><a href="https://saudetrevo.com.br/">Conheça</a></li>
        <li><a href="https://saudetrevo.com.br/consultas/">Consultas</a></li>
        <li><a href="https://saudetrevo.com.br/exames/">Exames</a></li>
        <li><a href="https://saudetrevo.com.br/exames/">Cirugias</a></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
.header {
  display: flex;
  align-items: center;
  gap: 20px;
}

.nav ul {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
  list-style-type: none;
}

.nav ul a {
  text-decoration: none;
  color: #5d4a64;
  font-size: 1rem;
}

.nav ul a:hover {
  font-weight: 600;
}
</style>
