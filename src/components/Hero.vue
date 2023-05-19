<template>
  <section class="hero">
    <div class="hero-image">
      <picture>
        <source media="(max-width: 1439px)" :srcset="bgIntroMobile">
        <source media="(min-width: 1440px)" :srcset="bgIntroDesktop">
        <img :src="bgIntroMobile" alt="Background Intro" class="hero-background">
      </picture>
      <img :src="imageMockups" alt="Mockup" class="hero-mockup">
    </div>
    <div class="hero-text">
      <h3 class="hero-title">Next generation digital banking</h3>
      <p class="hero-description">
        Take your financial life online. yourEasyBank account will be a one-stop-shop for spending, saving, budgeting, investing, and much more.
      </p>

      <button class="hero-cta">Request Invite</button>
    </div>
  </section>
</template>

<script>
import bgIntroMobile from '../assets/img/bg-intro-mobile.svg';
import bgIntroDesktop from '../assets/img/bg-intro-desktop.svg';
import imageMockups from '../assets/img/image-mockups.png';

export default {
  data() {
    return {
      bgIntroMobile,
      bgIntroDesktop,
      imageMockups
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

.hero {
  @include desktop {
    display: flex;
    flex-direction: row-reverse;
    padding: 0 8rem;
    z-index: 1;
    overflow: hidden;
  }
}

.hero-image  {
  position: relative;
  z-index: -1;
  
  @include desktop {
    width: 100%;
    z-index: 1;
  }
}

.hero-background {
  width: 100%;
  padding: 0;

  @include desktop {
    width: 150%;
    position: relative;
    top: -20%;
    right: -20%;
  }
}

.hero-mockup {
  display: block;
  position: absolute;
  left: 0;
  right: 0;
  top: -6rem;
  width: 90%;
  margin: auto;

  @include desktop {
    left:auto;
    right: -33%;
    top: -7rem;

  }
}

.hero-text {
  width: 90%;
  margin: -3.5rem auto 0;

  @include desktop {
    width: 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-top: 15rem;
  }
}

.hero-title {
  color: var(--dark-blue);
  font-weight: 300;
  text-align: center;

  @include desktop {
    font-size: 44px;
    text-align: start;
  }
}

.hero-description {
  color: var(--grayish-blue);
  text-align: center;
  margin-top: 2rem;
  line-height: 27px;

  @include desktop {
    text-align: start;
  }
}

.hero-cta {
  display: block;
  margin: 2rem auto 5rem;
  border-radius: 1.5rem;
  width: 150px;
  height: 40px;
  border: none;
  color: #fff;
  background-image: linear-gradient(to right, var(--lime-green), var(--bright-cyan));
  font-weight: 700;

  @include desktop {
    margin: 2rem 0 5rem;
  }
}
</style>