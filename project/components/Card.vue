<template>
  <div class="Container">
    <div class="Card">
      <h2>{{ Name }}</h2>
      <h2>Ability: {{ Ability }}</h2>
      <img class="Img" :src="Image" alt="Alt" />
      <div></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    Name: String,
    Ability: String,
    Image: String,
  },
}
</script>

<style>
h2 {
  color: #ffffff;
}
.Img {
  width: 18%;
  opacity: 1;
}
.Card {
  align-items: center;
  margin-bottom: 1%;
}
</style>