<template>
  <div class="donate-card">
    <img :src="image" />
    <section>
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
    </section>
    <button @click="onDonateBtnClick">{{ buttonText }}</button>
  </div>
</template>

<script>
export default {
  name: 'donate-card',
  props: {
    image: {
      type: String,
      default: 'https://placekitten.com/250/125',
    },
    title: {
      type: String,
      default: 'Card Title',
    },
    description: {
      type: String,
      default: 'lorem ipsum',
    },
    buttonText: {
      type: String,
      default: 'button',
    },
  },
  methods: {
    onDonateBtnClick() {
      this.$emit('donateBtnClick');
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.donate-card {
  border: 1px solid rgba(0, 0, 0, 0.125);
  width: 250px;
  height: 300px;
  margin: 5px;
}

section {
  padding: 0 1rem;
}

button {
  display: block;
  width: calc(100% - 2rem);
  background: #3541e0;
  border: 0;
  border-radius: 3px;
  color: #fff;
  cursor: pointer;
  padding: 10px;
  margin: 5px 1rem;
}
</style>
