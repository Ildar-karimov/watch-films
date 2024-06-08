<template>
  <MainLayout>
    <template #header>
      <PageHeader />
    </template>

    <template #navbar>
      <PageSideBar />
    </template>

    <template #default>
      <PageBody>
        <RouterView />

        <template #footer>
          <PageFooter />
        </template>
      </PageBody>
    </template>
  </MainLayout>
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router'

import { PageHeader } from '@/widgets/PageHeader';
import { PageSideBar } from '@/widgets/PageSideBar';
import { PageFooter } from '@/widgets/PageFooter';
import { PageBody } from '@/widgets/PageBody';
import { MainLayout } from '@/shared/ui/layouts';
</script>
