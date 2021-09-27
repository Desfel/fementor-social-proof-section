<template>
  <div class="page-wrapper">
    <div class="top-content">
      <div class="left-content">
        <h1>
          10,000+ of our users love our products.
        </h1>
        <p>
          We only provide great products combined with excellent customer
          service. See what our satisfied customers are saying about our
          services.
        </p>
      </div>

      <div class="right-content">
        <div class="rating-content">
          <div class="rating-stars">
            <span class="rating-star"></span>
            <span class="rating-star"></span>
            <span class="rating-star"></span>
            <span class="rating-star"></span>
            <span class="rating-star"></span>
          </div>

          <p>
            Rated 5 Stars in Reviews
          </p>
        </div>

        <div class="rating-content">
          <div class="rating-stars">
            <span class="rating-star"></span>
            <span class="rating-star"></span>
            <span class="rating-star"></span>
            <span class="rating-star"></span>
            <span class="rating-star"></span>
          </div>

          <p>
            Rated 5 Stars in Report Guru
          </p>
        </div>

        <div class="rating-content">
          <div class="rating-stars">
            <span class="rating-star"></span>
            <span class="rating-star"></span>
            <span class="rating-star"></span>
            <span class="rating-star"></span>
            <span class="rating-star"></span>
          </div>

          <p>
            Rated 5 Stars in BestTech
          </p>
        </div>
      </div>
    </div>

    <div class="bottom-content">
      <div class="quote-card">
        <div class="quote-author">
          <img src="@/assets/img/image-colton.jpg" alt="Colton Smith" />

          <div class="author-content">
            <p class="author-name">Colton Smith</p>
            <p class="author-status">Verified Buyer</p>
          </div>
        </div>

        <p class="quote-content">
          "We needed the same printed design as the one we had ordered a week
          prior. Not only did they find the original order, but we also received
          it in time. Excellent!"
        </p>
      </div>
      <div class="quote-card">
        <div class="quote-author">
          <img src="@/assets/img/image-irene.jpg" alt="Irene Roberts" />

          <div class="author-content">
            <p class="author-name">Irene Roberts</p>
            <p class="author-status">Verified Buyer</p>
          </div>
        </div>

        <p class="quote-content">
          "Customer service is always excellent and very quick turn around.
          Completely delighted with the simplicity of the purchase and the speed
          of delivery."
        </p>
      </div>
      <div class="quote-card">
        <div class="quote-author">
          <img src="@/assets/img/image-anne.jpg" alt="Anne Wallace" />

          <div class="author-content">
            <p class="author-name">Anne Wallace</p>
            <p class="author-status">Verified Buyer</p>
          </div>
        </div>

        <p class="quote-content">
          "Put an order with this company and can only praise them for the very
          high standard. Will definitely use them again and recommend them to
          everyone!"
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  head() {
    return {
      title: {
        inner: 'Home'
      },
      meta: [
        {
          name: 'description',
          content: `${this.appTitle} home page`,
          id: 'desc'
        }
      ]
    }
  },
  computed: mapState('app', ['appTitle'])
}
</script>

<style lang="scss" scoped>
@import '@/theme/variables.scss';

.page-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 127px 80px 100px;

  @media (max-width: 768px) {
    padding: 80px 24px;
  }

  .top-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    margin-bottom: 72px;

    @media (max-width: 768px) {
      flex-direction: column;
      text-align: center;
      margin-bottom: 49px;
    }

    .left-content {
      max-width: 35%;

      @media (max-width: 768px) {
        max-width: 100%;
      }

      h1 {
        margin-bottom: 20px;
        font-style: normal;
        font-weight: bold;
        font-size: 48px;
        line-height: 48px;
        letter-spacing: -1.71429px;
        color: $primaryColor1;

        @media (max-width: 768px) {
          font-size: 32px;
          line-height: 32px;
          text-align: center;
          letter-spacing: -1.14286px;
        }
      }

      p {
        font-style: normal;
        font-weight: 500;
        font-size: 15px;
        line-height: 25px;
        letter-spacing: -0.5px;
        color: $neutralColor1;
      }
    }

    .right-content {
      width: 100%;
      margin-left: 15%;
      flex-direction: column;

      @media (max-width: 768px) {
        align-items: center;
        justify-content: center;
        margin: 40px auto 0;
      }

      .rating-content {
        display: flex;
        max-width: 445px;
        margin: 0;
        padding: 20px 32px 15px;
        background: $neutralColor2;
        border-radius: 8px;
        text-align: center;

        @media (min-width: 769px) {
          &:nth-child(2) {
            margin-left: 48px;
          }

          &:last-child {
            margin-left: 96px;
          }
        }

        &:not(:last-child) {
          margin-bottom: 16px;
        }

        @media (max-width: 1024px) {
          flex-direction: column;
          align-items: center;
          justify-content: center;

          &:nth-child(2),
          &:last-child {
            margin-left: 0;
          }
        }

        @media (max-width: 768px) {
          max-width: 100%;
          margin: auto;

          &:nth-child(2),
          &:last-child {
            margin-left: auto;
            margin-right: auto;
          }
        }

        p {
          font-style: normal;
          font-weight: bold;
          font-size: 13px;
          line-height: 20px;
          color: $primaryColor1;
          margin-left: 32px;


          @media (max-width: 1024px) {
            margin-left: 0;
          }
        }

        .rating-stars {
          display: flex;

          @media (max-width: 1024px) {
            margin-bottom: 16px;
          }

          span {
            width: 17px;
            height: 16px;
            display: inline-block;
            margin-right: 9px;
            background: url('../assets/img/icon-star.svg') center no-repeat;
            background-size: cover;
          }
        }
      }
    }
  }

  .bottom-content {
    display: flex;
    justify-content: space-between;

    @media (max-width: 768px) {
      flex-direction: column;
    }

    .quote-card {
      position: relative;
      padding: 40px 32px;
      background: $primaryColor1;
      border-radius: 8px;

      &:not(:last-child) {
        margin-right: 30px;
      }

      @media (min-width: 769px) {
        &:nth-child(2) {
          top: 16px;
        }

        &:last-child {
          top: 32px;
        }
      }

      @media (max-width: 768px) {
        &:not(:last-child) {
          margin-right: 0;
          margin-bottom: 16px;
        }
      }
    }

    .quote-author {
      display: flex;
      margin-bottom: 26px;

      img {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        margin-right: 23px;
      }

      .author-name,
      .author-status {
        font-size: 13px;
        line-height: 15px;
      }

      .author-name {
        font-weight: bold;
        color: $neutralColor3;
        margin-bottom: 5px;
      }

      .author-status {
        color: $primaryColor2;
      }
    }

    .quote-content {
      font-weight: 500;
      font-size: 13px;
      line-height: 22px;
      letter-spacing: -0.232143px;
      color: $neutralColor3;
    }
  }
}
</style>
