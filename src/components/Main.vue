<template>
  <main>
    <!-- Home: Carousels -->
    <div id="homepage" class="main-container" v-if="emitText === ''">
      <!-- Comedy Carousel -->
      <h2>Film Comici</h2>
      <carousel :per-page="7" :loop="true" id="carousel-custom">
        <slide v-for="item in comedyArr" :key="item.id">
          <img
            :src="baseImageUrl + baseImageWidth + item.poster_path"
            alt="a"
          />
          <div class="back-card">
            <p class="title">{{ item.original_title }}</p>
            <p class="overview">{{ item.overview }}</p>
            <div class="stars">
              <div class="empty">
                <div class="inner">
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                </div>
              </div>

              <div class="solid" :style="`width:${6.7 * item.vote_average}px`">
                <div class="inner">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                </div>
              </div>
            </div>
          </div>
        </slide>
      </carousel>
      <!-- Drama Carousel -->
      <h2>Film Drammatici</h2>
      <carousel
        :per-page="7"
        :loop="true"
        :navigationClickTargetSize="8"
        id="carousel-custom"
      >
        <slide v-for="item in dramaArr" :key="item.id">
          <img
            :src="baseImageUrl + baseImageWidth + item.poster_path"
            alt="a"
          />
          <div class="back-card">
            <p class="title">{{ item.original_title }}</p>
            <p class="overview">{{ item.overview }}</p>
            <div class="stars">
              <div class="empty">
                <div class="inner">
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                </div>
              </div>

              <div class="solid" :style="`width:${6.7 * item.vote_average}px`">
                <div class="inner">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                </div>
              </div>
            </div>
          </div>
        </slide>
      </carousel>
      <!-- Thriller Carousel -->
      <h2>Film Thriller</h2>
      <carousel
        :per-page="7"
        :loop="true"
        :navigationClickTargetSize="8"
        id="carousel-custom"
      >
        <slide v-for="item in thrillerArr" :key="item.id">
          <img
            :src="baseImageUrl + baseImageWidth + item.poster_path"
            alt="a"
          />
          <div class="back-card">
            <p class="title">{{ item.original_title }}</p>
            <p class="overview">{{ item.overview }}</p>
            <div class="stars">
              <div class="empty">
                <div class="inner">
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                </div>
              </div>

              <div class="solid" :style="`width:${6.7 * item.vote_average}px`">
                <div class="inner">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                </div>
              </div>
            </div>
          </div>
        </slide>
      </carousel>
      <!-- Action Carousel -->
      <h2>Film d'Azione</h2>
      <carousel
        :per-page="7"
        :loop="true"
        :navigationClickTargetSize="8"
        id="carousel-custom"
      >
        <slide v-for="item in actionArr" :key="item.id">
          <img
            :src="baseImageUrl + baseImageWidth + item.poster_path"
            alt="a"
          />
          <div class="back-card">
            <p class="title">{{ item.original_title }}</p>
            <p class="overview">{{ item.overview }}</p>
            <div class="stars">
              <div class="empty">
                <div class="inner">
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                </div>
              </div>

              <div class="solid" :style="`width:${6.7 * item.vote_average}px`">
                <div class="inner">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                </div>
              </div>
            </div>
          </div>
        </slide>
      </carousel>
      <!-- Fantasy Carousel -->
      <h2>Film Fantasy</h2>
      <carousel
        :per-page="7"
        :loop="true"
        :navigationClickTargetSize="8"
        id="carousel-custom"
      >
        <slide v-for="item in fantasyArr" :key="item.id">
          <img
            :src="baseImageUrl + baseImageWidth + item.poster_path"
            alt="a"
          />
          <div class="back-card">
            <p class="title">{{ item.original_title }}</p>
            <p class="overview">{{ item.overview }}</p>
            <div class="stars">
              <div class="empty">
                <div class="inner">
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                </div>
              </div>

              <div class="solid" :style="`width:${6.7 * item.vote_average}px`">
                <div class="inner">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                </div>
              </div>
            </div>
          </div>
        </slide>
      </carousel>
    </div>
    <!-- Movie Results -->
    <h2
      class="main-container"
      v-if="emitText !== '' && results.movie.length > 0"
    >
      Film Trovati
    </h2>
    <div
      id="movie-results"
      class="main-container search-container"
      v-if="emitText !== '' && results.movie.length > 0"
    >
      <div v-for="movie in results.movie" :key="movie.id" class="card-search">
        <img
          v-if="movie.poster_path"
          :src="baseImageUrl + baseImageWidth + movie.poster_path"
          alt="alt"
        />
        <img
          v-else
          :src="require('../assets/img/image-not-available.png')"
          alt="not-available"
        />
        <div class="back-card">
          <p class="title">{{ movie.original_title }}</p>
          <p class="overview">{{ movie.overview }}</p>
          <div class="stars">
            <div class="empty">
              <div class="inner">
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
              </div>
            </div>

            <div class="solid" :style="`width:${6.7 * movie.vote_average}px`">
              <div class="inner">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Tv Series Results -->
    <h2 class="main-container" v-if="emitText !== '' && results.tv.length > 0">
      Serie Tv Trovate
    </h2>
    <div
      id="tv-results"
      class="main-container search-container"
      v-if="emitText !== '' && results.tv.length > 0"
    >
      <div v-for="serie in results.tv" :key="serie.id" class="card-search">
        <img
          v-if="serie.poster_path"
          :src="baseImageUrl + baseImageWidth + serie.poster_path"
          alt="alt"
        />
        <img
          v-else
          :src="require('../assets/img/image-not-available.png')"
          alt="not-available"
        />
        <div class="back-card">
          <p class="title">{{ serie.original_name }}</p>
          <p class="overview">{{ serie.overview }}</p>
          <div class="stars">
            <div class="empty">
              <div class="inner">
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
              </div>
            </div>

            <div class="solid" :style="`width:${6.7 * serie.vote_average}px`">
              <div class="inner">
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
                <i class="fas fa-star"></i>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import axios from "axios";

export default {
  name: "Main",
  props: ["emitText", "emitType"],
  data() {
    return {
      baseImageUrl: "https://image.tmdb.org/t/p/",
      baseImageWidth: "w200",
      apiHomeUrl: "https://api.themoviedb.org/3/discover/",
      /* array per i carousels di ogni genere */
      comedyArr: [],
      dramaArr: [],
      thrillerArr: [],
      fantasyArr: [],
      actionArr: [],
      /* array per ricerca avanzata */
      apiSearchUrl: "https://api.themoviedb.org/3/search/",
      results: {
        movie: [],
        tv: [],
      },
      apiKey: "dc976da41141e1736442fc8a7c438e96",
      query: "",
      type: "movie",
      /* data per carousel */
      visibleSlides: 5,
      indexSlide: 0,
      loaded: false,
    };
  },
  methods: {
    getHomeFilm() {
      //Data per Carousels, film e serie in evidenza, e divisi per categorie.
      this.getGenreFilms(this.comedyArr, 35);
      /* console.log("comedy:", this.comedyArr); */
      this.getGenreFilms(this.dramaArr, 18);
      /* console.log("drama:", this.dramaArr); */
      this.getGenreFilms(this.thrillerArr, 53);
      /* console.log("thriller:", this.thrillerArr); */
      this.getGenreFilms(this.fantasyArr, 14);
      /* console.log("fantasy:", this.fantasyArr); */
      this.getGenreFilms(this.actionArr, 28);
      /* console.log("action:", this.actionArr); */
    },
    getGenreFilms(genreArr, genre) {
      axios
        .get(this.apiHomeUrl + this.type, {
          params: {
            api_key: this.apiKey,
            with_genres: genre,
            sort_by: "popularity.desc",
          },
        })
        .then((res) => {
          /* console.log("dati in arrivo: ", res.data.results); */
          genreArr.splice(0, genreArr.length, ...res.data.results);
        })
        .catch((err) => {
          console.log(err);
        });
    },
    getResearchData() {
      this.resetResearch();
      if (this.emitText !== "") {
        if (this.emitType === "all") {
          this.getApiData("movie");
          this.getApiData("tv");
        } else {
          this.getApiData(this.emitType);
        }
      }
    },
    getApiData(type) {
      /* if (this.emitText !== "") { */
      axios
        .get(this.apiSearchUrl + type, {
          params: {
            api_key: this.apiKey,
            query: this.emitText,
            language: "it-IT",
          },
        })
        .then((res) => {
          console.log("dati in arrivo: ", res.data.results);
          this.results[type] = res.data.results;
          console.log(`array ${type} :`, this.results[type]);
        })
        .catch((err) => {
          console.log(err);
        });
      /* } */
    },
    resetResearch() {
      this.results.movie = [];
      this.results.tv = [];
    },
  },
  created() {
    this.getHomeFilm();
  },
  watch: {
    emitText: function() {
      this.getResearchData();
    },
    emitType: function() {
      this.getResearchData();
    },
  },
};
</script>

<style lang="scss" scoped>
main {
  padding: 50px;
}

.main-container {
  max-width: 1440px;
  margin: 0 auto;
  h2 {
    text-transform: uppercase;
    margin-bottom: 1rem;
  }
}

h2.main-container {
  text-transform: uppercase;
  margin-top: 1rem;
  margin-bottom: 1rem;
}

div.VueCarousel-slide {
  position: relative;
  img {
    width: 200px;
    height: 300px;
  }
}

.back-card {
  z-index: 999;
  position: absolute;
  top: 0;
  visibility: hidden;
  width: 200px;
  height: 300px;
  padding: 1rem;
  border: 1px solid white;
  transition: transform 0.4s linear;
  .title {
    height: 15%;
    overflow-y: auto;
    text-align: center;
    font-weight: 800;
    text-transform: uppercase;
    margin-bottom: 0.3rem;
  }
  .overview {
    height: 70%;
    margin-bottom: 0.75rem;
    overflow-y: auto;
  }
}

div.VueCarousel-slide:hover {
  visibility: hidden;
  .back-card {
    visibility: visible;
  }
}

.stars {
  position: relative;
  margin-bottom: 15px;
  font-size: 0.75rem;

  .solid {
    color: yellow;
    position: absolute;
    top: 0;
    left: 0;
    overflow: hidden;
  }
  .inner {
    width: 68px;
  }
}

/* Movie */
.search-container {
  display: grid;
  grid-template-columns: 50%;
  row-gap: 10px;
  img {
    width: 200px;
    height: 300px;
    border-radius: 3px;
  }
}

.card-search {
  position: relative;
}
.card-search:hover {
  visibility: hidden;
  .back-card {
    visibility: visible;
  }
}

/* button.VueCarousel-dot.VueCarousel-dot--active {
  background-color: cyan !important;
} */

/* media queries */

@media all and (min-width: 481px) and (max-width: 760px) {
  .search-container {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media all and (min-width: 761px) and (max-width: 950px) {
  .search-container {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media all and (min-width: 951px) and (max-width: 1250px) {
  .search-container {
    grid-template-columns: repeat(4, 1fr);
  }
}

@media all and (min-width: 1251px) and (max-width: 1500px) {
  .search-container {
    grid-template-columns: repeat(5, 1fr);
  }
}

@media all and (min-width: 1501px) {
  .search-container {
    grid-template-columns: repeat(6, 1fr);
  }
}

/* LOADER */

.lds-roller {
  display: inline-block;
  position: relative;
  width: 80px;
  height: 80px;
}
.lds-roller div {
  animation: lds-roller 1.2s cubic-bezier(0.5, 0, 0.5, 1) infinite;
  transform-origin: 40px 40px;
}
.lds-roller div:after {
  content: " ";
  display: block;
  position: absolute;
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: #fff;
  margin: -4px 0 0 -4px;
}
.lds-roller div:nth-child(1) {
  animation-delay: -0.036s;
}
.lds-roller div:nth-child(1):after {
  top: 63px;
  left: 63px;
}
.lds-roller div:nth-child(2) {
  animation-delay: -0.072s;
}
.lds-roller div:nth-child(2):after {
  top: 68px;
  left: 56px;
}
.lds-roller div:nth-child(3) {
  animation-delay: -0.108s;
}
.lds-roller div:nth-child(3):after {
  top: 71px;
  left: 48px;
}
.lds-roller div:nth-child(4) {
  animation-delay: -0.144s;
}
.lds-roller div:nth-child(4):after {
  top: 72px;
  left: 40px;
}
.lds-roller div:nth-child(5) {
  animation-delay: -0.18s;
}
.lds-roller div:nth-child(5):after {
  top: 71px;
  left: 32px;
}
.lds-roller div:nth-child(6) {
  animation-delay: -0.216s;
}
.lds-roller div:nth-child(6):after {
  top: 68px;
  left: 24px;
}
.lds-roller div:nth-child(7) {
  animation-delay: -0.252s;
}
.lds-roller div:nth-child(7):after {
  top: 63px;
  left: 17px;
}
.lds-roller div:nth-child(8) {
  animation-delay: -0.288s;
}
.lds-roller div:nth-child(8):after {
  top: 56px;
  left: 12px;
}
@keyframes lds-roller {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
