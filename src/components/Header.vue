<template>
  <header>
    <div class="header-content">
      <a href="/" class="home-link">
        <!-- <img src="../assets/img/logo-cinema.jpg" alt="cinema-logo" /> -->
        <i class="fas fa-video fa-4x"></i>
        <h1>Cinema &amp; TV</h1>
      </a>
      <div class="advanced-search">
        <input v-model.trim="textToSearch" type="text" placeholder="Cerca..." />
        <label for="filter">
          Filtra per..
        </label>
        <select name="filter" id="filter" v-model="typeSelected">
          <option value="all">Filtra...</option>
          <option value="movie">Film</option>
          <option value="tv">Serie</option>
        </select>
        <i class="fas fa-search search-custom" @click="emitData()"></i>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      /* default  */
      typeSelected: "all",
      textToSearch: "",
    };
  },
  methods: {
    emitData() {
      this.$emit("sendEmit", {
        text: this.textToSearch,
        type: this.typeSelected,
      });
    },
  },
};
</script>

<style lang="scss" scoped>
header {
  color: white;
  height: 100px;
  background-color: black;
  padding: 50px;
}

.header-content {
  max-width: 1440px;
  height: 100%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  img {
    width: 100px;
    height: 100px;
  }
}

.home-link {
  display: flex;
  align-items: center;
  transition: all 1.5s;

  &:hover {
    color: cyan;
    border-bottom: 5px solid cyan;
  }
  i {
    display: none;
  }
  h1 {
    display: none;
    margin-left: 1rem;
  }
}

.advanced-search input {
  width: 100px;
  height: 2rem;
  border-radius: 7px;
  padding-left: 1rem;
  margin-right: 1rem;
  &:focus {
    outline: none;
  }
}

.advanced-search label {
  display: none;
  margin-right: 1rem;
}

.advanced-search select {
  width: 100px;
  height: 2rem;
  border-radius: 7px;
  padding-left: 1rem;
  margin-right: 1rem;
  &:focus {
    outline: none;
  }
}

.advanced-search .search-custom {
  cursor: pointer;
  font-size: 1.3em;
  transition: all 1.5s;
  &:hover {
    color: cyan;
  }
}

/* media queries */

@media all and (min-width: 540px) {
  .home-link i {
    display: block;
  }
}

@media all and (min-width: 700px) and (max-width: 1024px) {
  .advanced-search input,
  .advanced-search select {
    width: 150px;
  }
}

@media all and (min-width: 900px) {
  .advanced-search label {
    display: inline-block;
  }
}

@media all and (min-width: 1025px) {
  .home-link h1 {
    display: block;
  }

  .advanced-search input,
  .advanced-search select {
    width: 200px;
  }
}
</style>
