<template>
  <footer>
    <div class="footer-divider">
      <div class="logo-wrapper">
        <img :src="logoImg" alt="Logo">
      </div>
      <div class="social-wrapper">
        <img :src="facebookIcon" alt="facebook">
        <img :src="youtubeIcon" alt="youtube">
        <img :src="twitterIcon" alt="twitter">
        <img :src="pinterestIcon" alt="pinterest">
        <img :src="instagramIcon" alt="instagram">
      </div>
    </div>

    <div class="footer-divider">
      <ul class="footer-links">
        <div class="links-divider">
          <li class="footer-link">
            <a href="">About Us</a>
          </li>
          <li class="footer-link">
            <a href="">Contact</a>
          </li>
          <li class="footer-link">
            <a href="">Blog</a>
          </li>
        </div>
        <div class="links-divider">
          <li class="footer-link">
            <a href="">Careers</a>
          </li>
          <li class="footer-link">
            <a href="">Suport</a>
          </li>
          <li class="footer-link">
            <a href="">Privacy policy</a>
          </li>
        </div>
      </ul>
    </div>
    

    <div class="footer-divider">
      <button class="hero-cta">Request Invite</button>

      <p>&copy; Easybank. All Rights Reserved.</p>
    </div>
  </footer>
</template>

<script>
import logoImg from '../assets/img/logo-white.svg';
import facebookIcon from '../assets/img/icon-facebook.svg';
import youtubeIcon from '../assets/img/icon-youtube.svg';
import twitterIcon from '../assets/img/icon-twitter.svg';
import pinterestIcon from '../assets/img/icon-pinterest.svg';
import instagramIcon from '../assets/img/icon-instagram.svg';

export default {
  data() {
    return {
      logoImg,
      facebookIcon,
      youtubeIcon,
      twitterIcon,
      pinterestIcon,
      instagramIcon
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

  footer {
    background-color: var(--dark-blue);
    padding: 2rem 0;

    @include desktop {
      padding: 2rem 8rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  }

  .logo-wrapper {
    display: flex;
    justify-content: center;
    margin: 1rem 0 2rem;
  }

  .social-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: .8rem;
    margin-bottom: 2rem;

    img {
      width: 26px;
    }
  }

  .footer-links {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    a {
      color: #fff;
      text-decoration: none;
    }

    @include desktop {
      flex-direction: row;
      gap: 10rem;
    }
  }

  li {
    margin-bottom: 1rem;
  }

  p {
    text-align: center;
    color: var(--grayish-blue);
  }

  .footer-divider {
    text-align: center;
  }

  .hero-cta {
    display: block;
    margin: 2.5rem auto 1.5rem;
    border-radius: 1.5rem;
    width: 150px;
    height: 40px;
    border: none;
    color: #fff;
    background-image: linear-gradient(to right, var(--lime-green), var(--bright-cyan));
    font-weight: 700;
  }
</style>