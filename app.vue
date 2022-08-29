<template>
  <div>
    <form
      id="app"
      @submit="checkForm"
      action="https://vuejs.org/"
      method="post"
    >
      <div>
        <label for="name">Nombre</label>
        <input
          id="name"
          name="name"
          type="text"
          v-model="name"
          placeholder="Your name"
        />
      </div>
      <div>
        <label for="age">Age</label>
        <input
          type="number"
          id="age"
          name="age"
          v-model="age"
          min="0"
          placeholder="Your age"
        />
      </div>
      <div>
        <label for="movie">Movie</label>
        <select v-model="movie" id="movie" name="movie">
          <option>Star Wars</option>
          <option>Vanilla Sky</option>
          <option>Atomic Blonde</option>
        </select>
      </div>
      <input type="submit" value="Send" />
    </form>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: null,
      age: null,
      movie: null,
      errors: [],
    };
  },
};
</script>
