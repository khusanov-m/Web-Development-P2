<template>
  <section class="container volunteer" id="volunteer">
    <div class="volunteer-content">
      <h2>Volunteer Your Valuable Time</h2>

      <div class="volunteer-content__text">
        <p>
          Say, “Yes, I am here,” to a lonely shelter kitty or puppy. We can all
          use a little scratch behind the ears. Donate your time to help the
          animals! Opportunities include dog walking, puppy and kitty petting,
          yard sale assistance, fundraising, community outreach, and more. Your
          valuable gift of time will have a positive impact on our community.
        </p>

        <p>
          All of our volunteers are wonderful people just like you. As an
          advocate for animal welfare you will have many two legged and four
          legged friends! Say, “Yes, I am here,” and volunteer today.
        </p>
      </div>

      <a href="#volunteer" class="volunteer-content__link"
        >Volunteer today <i class="fas fa-arrow-right"></i
      ></a>

      <div class="volunteer-testimonial">
        <img src="../assets/second-testimony.png" alt="testimonial" />
        <div class="volunteer-testimonial__text">
          <p class="volunteer-testimonial__text-comment">
            “It was incredible to see the selfless Mariposa SPCA workers
            volunteer their time to my well-being and general happiness. They’ve
            had an incredible impact on our community.”
          </p>
          <p class="volunteer-testimonial__text-author">
            Whiskers, Long-Haired Tabby
          </p>
        </div>
      </div>
      <div class="volunteer-testimonial">
        <img src="../assets/third-testimony.png" alt="testimonial" />
        <div class="volunteer-testimonial__text">
          <p class="volunteer-testimonial__text-comment">
            “It was remarkable to see not only the impact that volunteering had
            on myself, but also the impact delivered to all of the rescued
            animals.”
          </p>
          <p class="volunteer-testimonial__text-author">
            Parker Henderson, Human
          </p>
        </div>
      </div>
    </div>

    <div class="volunteer-imgs">
      <img src="../assets/second_pets-1.png" alt="dog" />
      <img src="../assets/second_pets-2.png" alt="cat" />
      <img src="../assets/second_pets-3.png" alt="dog" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.volunteer {
  position: relative;
  margin-top: 37.6rem;
  display: flex;
  justify-content: space-between;

  &-imgs {
    display: flex;
    position: relative;
    top: -7rem;

    img {
      position: absolute;
      z-index: 2;
      right: 4.2rem;
      transition: 0.2s ease;

      &:hover {
        z-index: 4;
        transform: scale(1.1);
      }

      &:nth-child(2) {
        right: 20rem;
        top: 17rem;
        z-index: 3;
      }
      &:nth-child(3) {
        top: 29.5rem;
        right: 0;
        z-index: 1;

        &:hover {
          z-index: 3;
          transform: scale(1.1);
        }
      }
    }
  }

  &-content {
    h2 {
      font-size: 6.4rem;
      font-weight: 600;
      color: #fff;
      line-height: 77px;
      max-width: 55rem;
      margin-bottom: 5rem;
    }
    &__text {
      color: rgba(255, 255, 255, 0.9);
      max-width: 64rem;
      margin-bottom: 4.6rem;

      p {
        margin-bottom: 3.8rem;
        font-weight: 500;
        font-size: 1.8rem;
      }
    }
    &__link {
      text-decoration: none;
      text-transform: uppercase;
      font-weight: 600;
      font-size: 1.8rem;
      line-height: 27px;
      color: rgba(253, 180, 97, 0.82);
      border-bottom: 2px solid rgba(253, 180, 97, 0.82);
      transition: 0.1s ease;

      i {
        font-style: italic;
      }

      &:hover {
        padding-bottom: 2px;
      }
    }
  }

  &-testimonial {
    margin-top: 12rem;
    display: flex;
    max-width: 64rem;

    img {
      width: 6.4rem;
      height: 6.4rem;
      margin-right: 2.4rem;
    }

    &__text {
      font-style: italic;
      font-size: 18px;

      &-comment {
        color: rgba(255, 255, 255, 0.9);
        margin-bottom: 2.4rem;
      }
      &-author {
        color: rgba(255, 255, 255, 0.6);
      }
    }
  }
}
</style>
