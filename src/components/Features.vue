<template>
  <section class="features">
    <h3 class="title">Why choose EasyBank?</h3>

    <p class="description">
      We levarage Open Banking to turn your bank account into your financial hub. Control your finances like never before!
    </p>
    <div class="features-wrapper">
    <div class="feature">
      <div class="feature-icon">
        <img :src="onlineIcon" alt="Icon">
      </div>

      <h5 class="feature-title">Online Banking</h5>
      <p class="feature-description">
        Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world!
      </p>
    </div>
    
    <div class="feature">
      <div class="feature-icon">
        <img :src="budgetingIcon" alt="Icon">
      </div>

      <h5 class="feature-title">Simple Budgeting</h5>
      <p class="feature-description">
        See exacly where your money goes each month. Receive notifications when you're close to your hitting limits!
      </p>
    </div>
    
    <div class="feature">
      <div class="feature-icon">
        <img :src="onBoardingIcon" alt="Icon">
      </div>

      <h5 class="feature-title">Fast Onboarding</h5>
      <p class="feature-description">
        We don't branches. Open your account in minutes online and start taking control of your finances right away!
      </p>
    </div>
    
    <div class="feature">
      <div class="feature-icon">
        <img :src="apiIcon" alt="Icon">
      </div>

      <h5 class="feature-title">Open API</h5>
      <p class="feature-description">
        Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier!
      </p>
    </div>
    </div>
  </section>
</template>

<script>
import onlineIcon from '../assets/img/icon-online.svg';
import budgetingIcon from '../assets/img/icon-budgeting.svg';
import onBoardingIcon from '../assets/img/icon-onboarding.svg';
import apiIcon from '../assets/img/icon-api.svg';

export default {
  data() {
    return {
      onlineIcon,
      budgetingIcon,
      onBoardingIcon,
      apiIcon
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

  .features {
    padding:  4rem 10%;
    margin: auto;
    text-align: center;
    background-color: var(--light-grayish-blue);

    @include desktop {
      padding: 8rem;
    }
  }

  .title {
    font-weight: 400;

    @include desktop {
      text-align: start;
    }
  }
  .description {
    margin-bottom: 5rem;
    
    @include desktop {
      font-size: 18px;    
      margin: 1.5rem 0 0;
      max-width: 50%;
    }
  }

  p {
    color: var(--grayish-blue);
    line-height: 27px;
    margin-top: 1.5rem;

    @include desktop {
      text-align: start;
    }
  }

  .features-wrapper {
    @include desktop {
      display: flex;
      gap: 1rem;
    }
  }

  .feature {
    margin: 2rem auto 1rem;
  }

  .feature-icon {
    margin: 1rem 0 1rem;

    @include desktop {
      text-align: start;
    }
  }

  .feature-title {
    font-weight: 300;

    @include desktop {
      text-align: start;
    }
  }
</style>