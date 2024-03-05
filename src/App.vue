<script setup>
import UnAmi from './components/UnAmi.vue'
</script>

<template>
  <div class="main p-3">
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/Arsenal_FC.svg" width='3%' class="logo vue" alt="Bootstrap logo" />
    </a>
    <un-ami unAmiName="Dr.Azerty" unAmiPhone="098765234" unAmiMail="a@a.aa" premium="1"></un-ami>
    <un-ami unAmiName="Cortex22" unAmiPhone="30303003" unAmiMail="cortex@cortex.cortex" premium="0"></un-ami>
    <un-ami unAmiName="Dr.Qwerty" unAmiPhone="098765234" unAmiMail="b@b.bb"></un-ami>
  </div>
</template>