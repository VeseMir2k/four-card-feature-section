<template>
  <article class="card" :class="class">
    <h2 class="card__title">{{ title }}</h2>
    <p class="card__description">{{ description }}</p>
    <img class="card__image" :src="image" alt="image" />
  </article>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    require: true,
  },
  description: {
    type: String,
    require: true,
  },
  image: {
    type: String,
    require: true,
  },
  class: {
    type: String,
    require: true,
  },
});
</script>

<style scoped>
.card {
  box-shadow: 0 15px 30px -11px rgba(131, 167, 210, 0.5);
  padding: 32px;
  position: relative;
  border-radius: 8px;
  overflow: hidden;
  height: 222px;
}

.card__image {
  position: absolute;
  right: 32px;
  bottom: 32px;
}

.supervisor::before,
.team-builder::before,
.karma::before,
.calculator::before {
  content: "";
  height: 4px;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
}

.supervisor::before {
  background-color: var(--cyan-color);
}
.team-builder::before {
  background-color: var(--red-color);
}
.karma::before {
  background-color: var(--orange-color);
}
.calculator::before {
  background-color: var(--blue-color);
}

@media (min-width: 1120px) {
  .card {
    height: 250px;
  }

  .supervisor {
    grid-column: 1 / span 1;
    grid-row: 2 / span 2;
  }

  .team-builder {
    grid-column: 2 / span 1;
    grid-row: 1 / span 2;
  }

  .karma {
    grid-column: 2 / span 1;
    grid-row: 3 / span 2;
  }

  .calculator {
    grid-column: 3 / span 1;
    grid-row: 2 / span 2;
  }
}
</style>
