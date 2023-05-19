<template>
  <section class="latest-articles">
    <h3>Latest Articles</h3>

    <div class="articles">
      <div class="article">
        <div class="article-thumbnail">
          <img :src="CurrencyImage" alt="Currency">
        </div>
        <div class="article-content">
          <small>By Claire Robinson</small>
          <h5 class="article-title">Receive money in any currencies with no fees!</h5>
          <p class="article-description">
            The world is getting smaller and we’re becoming more mobile. So why should you be forced to only receive money in a single …
          </p>
        </div>
      </div>
      
      <div class="article">
        <div class="article-thumbnail">
          <img :src="RestaurantImage" alt="Restaurant">
        </div>
        <div class="article-content">
          <small>By Wilson Hutton</small>
          <h5 class="article-title">Treat yourself without worrying about money!</h5>
          <p class="article-description">
            Our simple budgeting feature allows you to separate out your spending and set 
            realistic limits each month. That means you …
          </p>
        </div>
      </div>
      
      <div class="article">
        <div class="article-thumbnail">
          <img :src="PlaneImage" alt="Plane">
        </div>
        <div class="article-content">
          <small>By Wilson Hutton</small>
          <h5 class="article-title">Take your Easybank card wherever you go!</h5>
          <p class="article-description">
            We want you to enjoy your travels. This is why we don’t charge any fees on purchases while you’re abroad. We’ll even show you …
          </p>
        </div>
      </div>
      
      
      <div class="article">
        <div class="article-thumbnail">
          <img :src="ConfettiImage" alt="Plane">
        </div>
        <div class="article-content">
          <small>By Claire Robinson</small>
          <h5 class="article-title">Our invite-only Beta accounts are now live!</h5>
          <p class="article-description">
            After a lot of hard work by the whole team, we’re excited to launch our closed beta. It’s easy to request an invite through the site ...
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import CurrencyImage from '../assets/img/image-currency.jpg';
import RestaurantImage from '../assets/img/image-restaurant.jpg';
import PlaneImage from '../assets/img/image-plane.jpg';
import ConfettiImage from '../assets/img/image-confetti.jpg';

export default {
  data() {
    return {
      CurrencyImage,
      RestaurantImage,
      PlaneImage,
      ConfettiImage
    }
  }
}
</script>

<style lang="scss" scoped>
@mixin desktop {
  @media (min-width: 1440px) {
    @content;
  }
}

.latest-articles {
  & > h3 {
    text-align: center;
    font-weight: 300;
    margin: 6rem 0 2rem;
  }

  @include desktop {
    padding: 0 8rem;
  }
}

.articles {
  @include desktop {
    display: flex;
    gap: 1rem;

  }
}

.article {
  width: 90%;
  margin: auto;
  background-color: #fff;
  
  .article-content {
    padding: 1.5rem;
  }

  small {
    color: var(--grayish-blue);
  }

  @include desktop {
    margin: 0;
  }
}

.article-thumbnail {
  max-width: 100%;

  & img {
    width: 100%;
    border-top-right-radius: .8rem;
    border-top-left-radius: .8rem;
  }

  @include desktop {
    width: auto !important;
    max-height: 200px !important;
  }
}

.article-title {
  font-weight: 300;
  margin: 1rem 0;
}

.article-description {
  color: var(--grayish-blue);
  margin-bottom: 2rem;
}
</style>