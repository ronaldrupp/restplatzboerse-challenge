<template>
  <section class="container">
    <div class="header">
      <div class="title-container">
        <h1 class="title">Länder, Regionen, Orte</h1>
        <a href="#" class="link">Alle</a>
      </div>
      <p class="subtitle">Lorem Ispum Länder, Regionen, Orte</p>
    </div>
    <div class="destinations-container">
      <div class="white-overlay left"></div>
      <ul class="list-container">
        <li v-for="destination in destinations" :key="destination.text">
          <a :href="destination.link" class="destination-item">
            <img
              :src="destination.image"
              :alt="`Image of ${destination.text}`"
              class="destination-img"
            />
            <div class="destination-details">
              <span class="destination-details-name">
                {{ destination.text }}
              </span>
              <div class="destination-details-price-container">
                <span
                  class="destination-details-from"
                  v-if="destination.price > 0"
                >
                  ab
                </span>
                <span class="destination-details-price-tag">
                  {{ destination.price | price }}</span
                >
              </div>
            </div>
          </a>
        </li>
      </ul>
      <div class="white-overlay right"></div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    destinations: Array,
  },
  filters: {
    price: function (price) {
      if (price === 0) return "kostenlos";
      return `€ ${price}`;
    },
  },
};
</script>

<style lang="scss" scoped>
.header {
  padding: 0 19px;
}
.title-container {
  display: flex;
}
.title {
  font-size: 1.5rem;
  font-family: var(--title-font-family);
  font-weight: bold;
  color: var(--aqua-color);
  line-height: 30px;
  flex: 1;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
}
.subtitle {
  font-size: 1rem;
  font-family: var(--main-font-family);
  color: var(--greyish-color);
  line-height: 22px;
}
.link {
  color: var(--aqua-color);
  font-family: var(--main-font-family);
  line-height: 22px;
}
.destinations-container {
  position: relative;
}
.list-container {
  display: flex;
  overflow: auto;
  margin-top: 1.5em;
  position: relative;
  &::before {
    content: "";
    width: 23px;
    height: 100%;
    position: sticky;
    top: 0;
    left: 0;
    bottom: 0;
    background: linear-gradient(90deg, white, transparent);
  }
}
.white-overlay {
  width: 23px;
  height: 100%;
  position: absolute;
  top: 0;
  bottom: 0;
  z-index: 2;
}
.left {
  left: 0;
  background: linear-gradient(90deg, white, transparent);
}
.right {
  right: 0;
  background: linear-gradient(90deg, transparent, white);
}
.destination-item {
  width: 287px;
  height: 222px;
  border-radius: 15px;
  box-shadow: -2px 2px 0px var(--greenish-color);
  margin: 0px 19px 19px 19px;
  display: flex;
  flex-direction: column;
  .destination-img {
    object-fit: cover;
    width: 287px;
    height: 177px;
    border-radius: 15px 15px 0 0;
  }
  .destination-details {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 1em;
    flex: 1;
    .destination-details-name {
      color: var(--aqua-color);
      font-family: var(--main-font-family);
      font-weight: 700;
      line-height: 22px;
      text-overflow: ellipsis;
      overflow: hidden;
      white-space: nowrap;
      flex: 1;
    }
    .destination-details-price-container {
      color: var(--purple-color);
      font-family: var(--main-font-family);
      line-height: 22px;
      .destination-details-from {
        font-size: 0.75rem;
      }
      .destination-details-price-tag {
        font-family: var(--main-font-family);
        font-weight: 600;
      }
    }
  }
}
</style>
