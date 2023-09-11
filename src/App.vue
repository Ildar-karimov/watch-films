<script setup lang="ts">
import { RouterView } from 'vue-router'
import PageHeader from "@/components/layout/PageHeader.vue";
import PageSideBar from "@/components/layout/PageSideBar.vue";
import PageBody from "@/components/layout/PageBody.vue";
import PageFooter from "@/components/layout/PageFooter.vue";
</script>

<template>
  <div class="page">
    <PageHeader />
    <PageSideBar />
    <PageBody>
      <RouterView />
    </PageBody>
    <PageFooter />
  </div>
</template>
