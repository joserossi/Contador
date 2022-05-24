<template>
  <div class="container">
    <h1>{{ count }}</h1>
    <div class="alert alert-danger" role="alert" v-show="showalert">
      El número no puede ser negativo
    </div>
    <button @click="Restar" type="button" class="btn btn-danger m-1">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="currentColor"
        class="bi bi-dash-lg"
        viewBox="0 0 16 16"
      >
        <path
          fill-rule="evenodd"
          d="M2 8a.5.5 0 0 1 .5-.5h11a.5.5 0 0 1 0 1h-11A.5.5 0 0 1 2 8Z"
        />
      </svg>
    </button>
    <button @click="Sumar" type="button" class="btn btn-success m-1">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="currentColor"
        class="bi bi-plus-lg"
        viewBox="0 0 16 16"
      >
        <path
          fill-rule="evenodd"
          d="M8 2a.5.5 0 0 1 .5.5v5h5a.5.5 0 0 1 0 1h-5v5a.5.5 0 0 1-1 0v-5h-5a.5.5 0 0 1 0-1h5v-5A.5.5 0 0 1 8 2Z"
        />
      </svg>
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
      showalert: false,
    };
  },
  methods: {
    Sumar() {
      this.count++;
      this.showalert = false;
    },
    Restar() {
      if (this.count > 0) return this.count--;
      else this.showalert = true;
    },
  },
};
</script>

<style>
</style>