<template>
  <section class="section">
    <span class="results">Encontramos <b>13</b> resultados</span>
    <ul class="container">
      <Card
        icon="https://cdn.saudetrevo.com.br/logos/laboratory/isa-lab-square.png"
        title="IsaLab"
        subTitle="Unidade Santo Antônio"
        price="123.78"
        inLab
        isTrevoPattern
      />

      <Card
        icon="https://cdn.saudetrevo.com.br/logos/laboratory/Logo_portinari.jpg"
        title="Portinari/ St Patrick"
        subTitle="Unidade Centro"
        price="93.80"
        inLab
        inHome
      />
      <Card
        icon="https://cdn.saudetrevo.com.br/logos/laboratory/transduson_logo.jpg"
        title="Transduson"
        subTitle="Unidade Leste"
        price="456.00"
        inHome
      />
      <Card
        icon="https://cdn.saudetrevo.com.br/logos/laboratory/isa-lab-square.png"
        title="IsaLab"
        subTitle="Unidade Norte"
        price="123.78"
        inLab
      />
      <Card
        icon="https://cdn.saudetrevo.com.br/logos/laboratory/logo-labi-square.png"
        title="Labi"
        subTitle="Unidade Centro"
        price="132.25"
        inHome
      />
    </ul>
  </section>
</template>

<style scoped>
.results {
  color: #695673;
  padding: 5px 0;
  opacity: 0.8;
  font-size: 1rem;
}

.section {
  margin-top: 6px;
}

.container {
  display: flex;
  flex-direction: column;
  gap: 10px;
  background: #eee;
  padding: 15px;
  list-style-type: none;
  margin: 5px 0;
  border-radius: 10px;
}
</style>
