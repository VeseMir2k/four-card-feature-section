<template>
  <Header />
  <main class="main">
    <Card
      title="Supervisor"
      description="Monitors activity to identify project roadblocks"
      :image="supervisorIcon"
      class="supervisor"
    />

    <Card
      title="Team Builder"
      description="Scans our talent network to create the optimal team for your project"
      :image="teamBuilderIcon"
      class="team-builder"
    />

    <Card
      title="Karma"
      description="Regularly evaluates our talent to ensure quality"
      :image="karmaIcon"
      class="karma"
    />

    <Card
      title="Calculator"
      description="Uses data from past projects to provide better delivery estimates"
      :image="calculatorIcon"
      class="calculator"
    />
  </main>
</template>

<script setup>
import Header from "./components/Header.vue";
import Card from "./components/Card.vue";
import supervisorIcon from "./images/icon-supervisor.svg";
import teamBuilderIcon from "./images/icon-team-builder.svg";
import karmaIcon from "./images/icon-karma.svg";
import calculatorIcon from "./images/icon-calculator.svg";
</script>

<style>
.main {
  display: grid;
  gap: 24px;
  margin-bottom: 80px;
}

@media (min-width: 1120px) {
  .main {
    width: 1110px;
    gap: 30px;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(4, 1fr);
  }
}
</style>
