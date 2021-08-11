<template>
  <section class="container adopting" id="adopting">
    <div class="adopting-imgs">
      <img src="../assets/first_pets-1.png" alt="dog" />
      <img src="../assets/first_pets-2.png" alt="cat" />
      <img src="../assets/first_pets-3.png" alt="dog" />
    </div>

    <div class="adopting-content">
      <h2>Finding a Forever Friend</h2>

      <div class="adopting-content__text">
        <p>
          Millions of companion animals in shelters across America are just
          waiting for a special home like yours. Navigating the adoption process
          isn't as hard as you think. We can help you find the perfect pet and
          discover how amazing adopting a pet can be.
        </p>

        <p>
          An animal shelter or a rescue group is the best source for a new pet,
          and our pet-care experts have compiled all the information you'll need
          to find your nearest group, select a pet who matches your lifestyle,
          and more.
        </p>
      </div>

      <a href="#adopting" class="adopting-content__link"
        >Start adopting <i class="fas fa-arrow-right"></i
      ></a>

      <div class="adopting-testimonial">
        <img src="../assets/first-testimony.png" alt="testimonial" />
        <div class="adopting-testimonial__text">
          <p class="adopting-testimonial__text-comment">
            “The Mariposa Team was invaluable to my adoption process, providing
            all the necesary matierals to ensure a smooth and safe process.”
          </p>
          <p class="adopting-testimonial__text-author">Fido, Pedigree Pug</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.adopting {
  padding-top: 49.4rem;
  display: flex;
  justify-content: space-between;

  &-imgs {
    display: flex;
    position: relative;

    img {
      position: absolute;
      z-index: 3;
      transition: 0.2s ease-in;

      &:hover {
        z-index: 5;
        transform: scale(1.1);
      }

      &:nth-child(2) {
        top: 12.4rem;
        left: 20rem;
        z-index: 2;

        &:hover {
          z-index: 3;
          transform: scale(1.1);
        }
      }
      &:nth-child(3) {
        top: 29.6rem;
        left: 4.2rem;
        z-index: 1;

        &:hover {
          z-index: 4;
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
