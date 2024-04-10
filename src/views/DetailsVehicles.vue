<template>
  <div class="p-9 md:flex md:justify-between">
    <div v-for="card in cards" :key="card.id">
      <card-details :data="card" />
    </div>
  </div>
</template>

<script>
import CardDetails from './components/CardDetails.vue'
export default {
  components: { CardDetails },
  data() {
    return {
      cards: [
        {
          id: 0,
          title: 'Proin in lorem tortor',
          subTitle:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce porta est a est rutrum ultricies. Etiam placerat id dui eget vestibulum. Praesent aliquam magna nunc, sit amet facilisis ante elementum quis. Curabitur tincidunt neque libero, at pretium nulla mattis ac. Morbi auctor lacus lectus, eget facilisis urna commodo sit amet.',
          img: '/assets/images/ford-2.png',
          isResponsive: true,
        },
        {
          id: 1,
          title: 'Proin in lorem tortor',
          subTitle:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce porta est a est rutrum ultricies. Etiam placerat id dui eget vestibulum. Praesent aliquam magna nunc, sit amet facilisis ante elementum quis. Curabitur tincidunt neque libero, at pretium nulla mattis ac. Morbi auctor lacus lectus, eget facilisis urna commodo sit amet.',
          img: '/assets/images/ford-3.png',
          isResponsive: true,
        },
        {
          id: 2,
          title: 'Proin in lorem tortor',
          subTitle:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce porta est a est rutrum ultricies. Etiam placerat id dui eget vestibulum. Praesent aliquam magna nunc, sit amet facilisis ante elementum quis. Curabitur tincidunt neque libero, at pretium nulla mattis ac. Morbi auctor lacus lectus, eget facilisis urna commodo sit amet.',
          img: '/assets/images/card-3.png',
          isResponsive: false,
        },
      ],
    }
  },
}
</script>

<style></style>
