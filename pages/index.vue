<template>
  <v-container fluid>
    <HeroImage />
    <v-container class="pb-10" max-width="1440px">
      <SectionTitle id="contents">業務内容</SectionTitle>
      <Features />
      <SectionTitle id="information">会社概要</SectionTitle>
      <CorporateInfo />
      <SectionTitle id="inquire">お問い合わせ</SectionTitle>
      <InquireForm />
    </v-container>
  </v-container>
</template>

<script setup lang="ts">
import HeroImage from '~/components/HeroImage.vue';
import SectionTitle from '~/components/SectionTitle.vue';
import Features from '~/components/Features/Features.vue';
import CorporateInfo from '~/components/Information/CorporateInfo.vue';
import InquireForm from '~/components/Inquire/InquireForm.vue';

</script>