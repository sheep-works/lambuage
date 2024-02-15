<template>
  <v-container fluid>
    <HeroImage />
    <section fluid style="max-width: 1440px; margin-left: auto; margin-right: auto;">
      <SectionTitle id="contents">業務内容</SectionTitle>
      <Features />
      <SectionTitle id="information">会社概要</SectionTitle>
      <CorporateInfo />
      <SectionTitle id="inquire">お問い合わせ</SectionTitle>
      <InquireForm />
    </section>
  </v-container>
</template>

<script setup lang="ts">
import HeroImage from '~/components/HeroImage.vue';
import SectionTitle from '~/components/SectionTitle.vue';
import Features from '~/components/Features/Features.vue';
import CorporateInfo from '~/components/Information/CorporateInfo.vue';
import InquireForm from '~/components/Inquire/InquireForm.vue';

</script>