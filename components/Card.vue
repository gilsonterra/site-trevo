<template>
  <li :class="isTrevoPattern ? 'card is-trevo-pattern' : 'card'">
    <div class="tag" v-if="isTrevoPattern">
      <IconCheck />
      Parceiro Trevo
    </div>
    <div class="img-container">
      <img :src="icon" :alt="title" height="70px" />
    </div>
    <div class="information">
      <div class="title">
        {{ title }}
      </div>
      <div class="subtitle">
        {{ subTitle }}
      </div>
    </div>
    <div class="address">
      <IconLocation />
      Rua Espírito Santo, 118 Santo Antônio São Caetano do Sul
    </div>

    <div class="extra-information">
      <div v-if="inHome">
        <IconHome />
        Coleta feita em casa
      </div>
      <div v-if="inLab">
        <IconLab />
        Atendimento somente no laboratório
      </div>
    </div>
    <div class="price">
      <div class="old">{{ oldPrice }}</div>
      <div class="new">{{ newPrice }}</div>
    </div>
  </li>
</template>

<script setup>
const props = defineProps({
  icon: String,
  title: String,
  subTitle: String,
  price: Number,
  isTrevoPattern: Boolean,
  inHome: Boolean,
  inLab: Boolean,
});

const oldPrice = computed(() => {
  return (props.price * 1.3).toLocaleString('pt-br', {
    style: 'currency',
    currency: 'BRL',
  });
});

const newPrice = computed(() => {
  return (props.price * 1).toLocaleString('pt-br', {
    style: 'currency',
    currency: 'BRL',
  });
});
</script>

<style scoped>
@keyframes animation-card {
  from {
    opacity: 0.9;
    transform: translateY(10px);
  }

  to {
    opacity: 1;
  }
}

@keyframes animation-title {
  from {
    transform: translateY(10px);
  }
}

@keyframes animation-img {
  from {
    opacity: 0.1;
  }
}

.card {
  position: relative;
  background: white;
  height: 70px;
  padding: 15px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 15px;
  border-radius: 10px;
  animation: animation-card 600ms;
}

.card:hover {
  background-image: linear-gradient(#bbaac1, #b09db7);
}

.img-container {
  animation: animation-img 1s;
}

.tag {
  background: #695673;
  color: white;
  font-weight: bold;
  padding: 2px 5px;
  border-bottom-right-radius: 5px;
  font-size: 0.7rem;
  position: absolute;
  top: 0px;
  left: 0px;
  display: flex;
  gap: 5px;
  align-items: start;
  justify-content: center;
  z-index: 3;
}

.card.is-trevo-pattern {
  border: solid 3px #695673;
}

.information {
  display: flex;
  flex-direction: column;
  align-items: start;
  justify-content: center;
  gap: 5px;
  flex: 1;
}

.information .title {
  font-weight: bold;
  font-size: 1.2rem;
  color: #695673;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 5px;
  animation: animation-title 600ms;
}

.information .subtitle {
  font-size: 0.9rem;
  font-style: italic;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 5px;
  animation: animation-title 1s;
}

.price {
  font-weight: bold;
  color: #695673;
  width: 120px;
  display: flex;
  justify-content: end;
  align-items: end;
  flex-direction: column;
  animation: animation-title 1s;
}

.price .old {
  font-size: 0.9rem;
  text-decoration: line-through;
  opacity: 0.6;
}

.price .new {
  font-size: 1.4rem;
}

.extra-information {
  display: flex;
  flex-direction: column;
  gap: 5px;
  width: 300px;
  animation: animation-title 1s;
}

.extra-information div {
  display: flex;
  align-items: center;
  justify-content: start;
  gap: 5px;
  color: #695673;
  font-size: 0.9rem;
  animation: animation-title 1s;
}

.address {
  padding: 10px;
  font-size: 0.9rem;
  color: #695673;
  width: 200px;
  animation: animation-title 1s;
}
</style>
