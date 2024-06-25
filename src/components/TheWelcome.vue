<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <div class="welcome-container">
    <WelcomeItem class="welcome-item">
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>PENDIDIKAN</template>
      <div class="content">
        PENDIDIKAN YANG DITEMPUH<br> SD (03 KuntoDarussalam)<br> SMP (SMPN 3 KuntoDarussalam)<br> SMK (SMKN PERTANIAN TERPADU)
      </div>
    </WelcomeItem>

    <WelcomeItem class="welcome-item">
      <template #icon>
        <ToolingIcon />
      </template>
      <template #heading>OTOMOTIF</template>
      <div class="content">
        Ketertarikan dengan dunia otomotif<br> mobil dan motor
      </div>
    </WelcomeItem>

    <WelcomeItem class="welcome-item">
      <template #icon>
        <EcosystemIcon />
      </template>
      <template #heading>GAMES</template>
      <div class="content">
        Games Favorite untuk saat ini,<br> 1. Mobile legends
      </div>
    </WelcomeItem>

    <WelcomeItem class="welcome-item">
      <template #icon>
        <CommunityIcon />
      </template>
      <template #heading>MEDIA SOSIAL</template>
      <div class="content">
        - Instagram : @hanindito___<br> - Tiktok : @hanindito___
      </div>
    </WelcomeItem>

    <WelcomeItem class="welcome-item">
      <template #icon>
        <SupportIcon />
      </template>
      <template #heading>DATA DIRI</template>
      <div class="content">
        1. NAMA : Bagas Nur Hanindito<br> 2. UMUR : 20<br> 3. KULIAH : Universitas Islam Riau<br> 4. JENIS KELAMIN : LAKI-LAKI
        <a href="https://vuejs.org/sponsor/" target="_blank" rel="noopener"></a>
      </div>
    </WelcomeItem>
  </div>
</template>

<style scoped>
:root {
  --primary-color: #42b983;
  --secondary-color: #35495e;
  --background-color: #f9f9f9;
  --accent-color: #ff4081;
  --font-family: 'Arial, sans-serif';
}

.welcome-container {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  max-width: 800px;
  margin: 2rem auto;
  font-family: var(--font-family);
}

.welcome-item {
  background-color: var(--background-color);
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.welcome-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}

.welcome-item .content {
  margin-top: 1rem;
  color: var(--secondary-color);
  line-height: 1.6;
}

.welcome-item h3 {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
  color: var(--primary-color);
}

@media (min-width: 768px) {
  .welcome-container {
    flex-direction: row;
    flex-wrap: wrap;
    gap: 2rem;
  }

  .welcome-item {
    flex: 1 1 calc(50% - 2rem);
    margin-bottom: 2rem;
  }
}
</style>
