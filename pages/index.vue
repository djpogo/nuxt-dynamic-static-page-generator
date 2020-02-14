<template>
  <div class="container">
    <ul>
      <li
        v-for="dog in dogs"
        :key="`dog-${dog.id}`"
      >
        <nuxt-link :to="`/${dog.id}`">
          {{ dog.id }}
        </nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  asyncData() {
    return axios.get('https://api.thedogapi.com/v1/images/search?limit=20&order=Desc')
      // eslint-disable-next-line arrow-body-style
      .then(({ data }) => {
        return {
          dogs: data,
        };
      });
  },
};
</script>
