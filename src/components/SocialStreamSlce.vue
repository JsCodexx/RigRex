<template>
    <section class="social-stream-section">
  
      <div class="social-stream-title">
        <h2> 
          <span>{{ slice.primary.title }}</span>
          <HeadingSuffix :color="slice.primary.suffix_color" margin-left="-1rem" /> 
        </h2>
      </div>
  
      <div class="social-stream-carousel" :class="isGettingSocialStreamData ? 'd-none' : ''">
  
        <div ref="carouselViewport" class="carousel-viewport transition">
          <div
            class="carousel-item cursor-pointer transition"
            v-for="(item, index) in socialStreamData"
            :key="index"
            @click="openModal(item.full_picture, item.message)"
          >
            <div class="image-container">
              <img :src="item.full_picture" alt="" />
            </div>
            <div class="carousel-item-info transition">
              <!-- <img src="@/assets/svg/icons/eye.svg" alt="Eye icon" class="carousel-item-eye-icon" /> -->
              <!-- <p class="carousel-item-description">{{ item.message && `${item.message.substr(0, 150)}...` }}</p> -->
            </div>
          </div>
        </div>
      </div>
      <div class="dot-navigation" :class="isGettingSocialStreamData ? 'd-none' : ''">
        <span
          v-for="(item, index) in socialStreamData"
          :key="index"
          @click="scrollToIndex(index)"
          :class="{ active: index === currentIndex }"
        ></span>
      </div>
      <button
        class="prev-btn transition"
        :class="isGettingSocialStreamData ? 'd-none' : ''"
        :data-disabled="currentIndex <= 0"
        @click="scrollToIndex(currentIndex - 1)"
      ></button>
      <button
        class="next-btn transition"
        :class="isGettingSocialStreamData ? 'd-none' : ''"
        :data-disabled="currentIndex >= (socialStreamData.length - ITEMS_PER_PAGE)"
        @click="scrollToIndex(currentIndex + 1)"
      ></button>
      <div
        class="modal-container transition"
        :style="{
          visibility: modalVisible ? 'visible' : 'hidden',
          opacity: modalVisible ? 1 : 0,
        }"
        @click="closeModal"
      >
        <div class="modal-content">
          <div class="modal-columns">
            <div class="left-column">
              <img class="modal-image" :src="full_picture" alt="Modal image" />
            </div>
            <div class="right-column">
              <div class="modal-description" v-html="message"></div>
            </div>
          </div>
        </div>
      </div>
  
  
    </section>
  </template>
  
  <script>
  // import { getSliceComponentProps } from "@prismicio/vue/components";
  // import HeadingSuffix from '~/components/common/HeadingSuffix.vue'
  
  export default {
    name: "SocialStreamSlice",
    // The array passed to `getSliceComponentProps` is purely optional and acts as a visual hint for you
    // props: getSliceComponentProps(["slice", "index", "slices", "context"]),
    components: {
      // HeadingSuffix
    },
  
    data() {
      return {
        currentIndex: 1,
        ITEMS_PER_PAGE: 3.6,
        ALL_ITEMS_SCROLL_WIDTH: 31.17,
        socialStreamData: [],
        full_picture: null,
        message: null,
        modalVisible: false,
        isGettingSocialStreamData: false
      }
    },
  
    mounted() {
      this.getSoicalStreamDetails()
      this.scrollToIndex(0)
      this.addWindowResizeEventListener()
      this.checkScreenWidth()
  
    },
  
    methods: {
      async getSoicalStreamDetails() {
        this.isGettingSocialStreamData = true
        const res = await this.$axios.get('/api/v1/socialstream')
        this.socialStreamData = res.data.data
        this.isGettingSocialStreamData = false
  
      },
  
  
      addWindowResizeEventListener() {
  
        window.addEventListener("resize", () => {
          this.checkScreenWidth()
        });
  
  
      },
  
      checkScreenWidth() {
        if (window.innerWidth < 599) {
          this.ITEMS_PER_PAGE = 1.4
          this.ALL_ITEMS_SCROLL_WIDTH = 72.62
        }
  
        if (window.innerWidth > 599 && window.innerWidth < 900) {
          this.ITEMS_PER_PAGE = 2.5
          this.ALL_ITEMS_SCROLL_WIDTH = 41.6
        }
  
        if (window.innerWidth > 900) {
          this.ITEMS_PER_PAGE = 3.6
          this.ALL_ITEMS_SCROLL_WIDTH = 31.17
        }
  
      },
  
  
      openModal(full_picture, message) {
        this.modalVisible = true
        this.full_picture = full_picture
        this.message = message
      },
      closeModal() {
        this.modalVisible = false
      },
  
        
      scrollToIndex(index) {
        this.currentIndex = index
        const carousel = this.$refs.carouselViewport
        carousel.style.transform = `translateX(-${this.ALL_ITEMS_SCROLL_WIDTH * index}%)`
      },
  
  
  
    }
  
  }
  </script>
  
  <style lang="scss">
  .social-stream-section {
  
    position: relative;
    margin-top: 14.45rem;
    @extend .boxedSection;
  
  
    @include for-phone-only {
      
    }
  
  
  
    .social-stream-title {
      h2 {
        font-family: $primaryFont;
        font-size: 5rem;
        font-weight: bold;
        color: $black;
        text-transform: uppercase;
        @include for-phone-only {    
          font-size: 2.8rem;
          font-weight: 900;
        }
  
  
        @include for-tablet-portrait-up {
          font-size: 3.8rem;
        }
  
        @include for-tablet-landscape-up {
          font-size: 5rem;
        }
  
      }
  
    }
  
    .social-stream-carousel {
      margin-top: 9rem;
      display: flex;
      overflow: hidden;
      position: relative;
      height: 65rem;
  
      .carousel-viewport {
        display: flex;
        height: 100%;
        width: 100%;
        position: absolute;
        left: 0;
        transform: translateX(0);
        .carousel-item {
          flex: 0 0 calc(100% / 3.6); /* show 3 items per row */
          position: relative;
          width: 27.77%;
          height: auto;
          margin: 0 2.5rem 0 2.5rem;
          .image-container {
            width: 100%;
            height: 42rem;
            clip-path: polygon(50% 0, 100% 23%, 100% 77%, 50% 100%, 0 77%, 0 23%);
            img {
              width: 100%;
              height: 100%;
              object-fit: cover;
            }
          }
    
          .carousel-item-info {
            opacity: 0;
            margin-top: 4.84rem;
            border-top: 0.2rem solid $blue;
            padding-top: 3.31rem;
    
            .carousel-item-eye-icon {
              width: 3.9rem;
              height: 2.5rem;
              object-fit: contain;
    
            }
            .carousel-item-description {
              margin-top: 1.8rem;
              font-family: $primaryFont;
              font-size: 1.6rem;
              font-weight: 300;
              line-height: 1.44;
              color: $black;
    
            }
    
    
          }
    
          &:hover .carousel-item-info {
            opacity: 1;
          }
    
    
    
          &:nth-child(1) {
            margin-left: 0;
          }
    
          @include for-phone-only {    
            flex: 0 0 calc(100% / 1.4); /* show 1 items per row */
            width: 71.42%;
            margin: 0 0.6% 0 0.6%;
            .image-container {
              width: 100%;
              height: 26.8rem;
            }
    
            .carousel-item-info {
              opacity: 1;
              margin-top: 3.05rem;
              padding-top: 2.12rem;
    
              .carousel-item-eye-icon {
                width: 2.4rem;
                height: 1.6rem;
              }
    
    
              .carousel-item-description {
                margin-top: 0.4rem;
                font-size: 1.4rem;
              }
    
    
    
            }
    
    
    
          }
  
          @include for-tablet-portrait-up {    
            flex: 0 0 calc(100% / 2.5); /* show 2 items per row */
            width: 40%;
            margin: 0 0.8% 0 0.8%;
            .image-container {
              height: 35rem;
            }
  
            .carousel-item-info {
              opacity: 1;
            }
          }
  
          @include for-tablet-landscape-up {    
            flex: 0 0 calc(100% / 3.6); /* show 3 items per row */
            width: 27.77%;
            margin: 0 1.7% 0 1.7%;
            .image-container {
              height: 42rem;
            }
  
            .carousel-item-info {
              opacity: 0;
            }
  
  
          }
    
        }
      }
      
  
      @include for-phone-only {    
        margin-top: 4.2rem;
        height: 50rem;
  
      }
  
  
  
      
    }
  
  
  
    .prev-btn,
    .next-btn {
      position: absolute;
      top: 41%;
      bottom: 0;
      width: 7.5rem;
      height: 7.5rem;
      opacity: 0.61;
      mix-blend-mode: lighten;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.2rem;
      background-color: $white;
      cursor: pointer;
      user-select: none;
      border-radius: 50%;
      overflow: hidden;
      border: none;
      @include for-phone-only {    
        top: 33%;
      }
  
      @include for-tablet-portrait-up {   
        top: 36%;
      }
  
      @include for-tablet-landscape-up {  
        top: 41%;
      }
  
  
  
    }
    
    .prev-btn {
      left: 0.5%;
      padding: 2rem 2rem 2rem 1.5rem;
    }
    
    .next-btn {
      right: 0.5%;
      padding: 2rem 2rem 2rem 2.5rem;
  
    }
    
    .prev-btn::before,
    .next-btn::before {
      content: "";
      display: block;
      width: 0;
      height: 0;
      border-style: solid;
      border-width: 1.625rem 2.5625rem 1.625rem 0;
      border-color: transparent $black transparent transparent;
    }
    
    .next-btn::before {
      border-width: 1.625rem 0 1.625rem 2.5625rem;
      border-color: transparent transparent transparent $black;
    }
    
    .prev-btn[data-disabled],
    .next-btn[data-disabled] {
      display: none;
    }
  
  
    .dot-navigation {
      display: none;
      justify-content: center;
      margin-top: 1rem;
  
      
      span {
        display: inline-block;
        width: 0.7rem;
        height: 0.7rem;
        background-color: $white;
        border: 0.2rem solid $black;      
        border-radius: 50%;
        margin: 0 0.25rem;
        cursor: pointer;
        &.active {
          padding: 0.2rem;
          background-color: $blue;
          border: 0.2rem solid $blue;      
        }
      }
  
  
      @include for-phone-only {    
        display: flex;
      }
  
  
    }
  
    .d-none {
      display: none;
    }
  
    .modal-container {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 1;
      background-color: rgba(0, 0, 0, 0.7);
      display: flex;
      align-items: center;
      justify-content: center;
      &:hover {
        visibility: visible;
        opacity: 1;
        cursor: pointer;
      }
      &:focus {
        visibility: hidden;
        opacity: 0;
      }
      .modal-content {
        max-width: 80%;
        max-height: 80%;
        height: auto;
        border-radius: 0.5rem;
        overflow: hidden;
      }
      .modal-columns {
        margin: 1rem;
        display: flex;
        .left-column {
          padding: 1rem;
          width: 50%;
          .modal-image {
            padding: 1rem;
            width: 100%;
            height: 100%;
            object-fit: cover;
          }
          @include for-phone-only {   
            width: 100%; 
          }
  
  
        }
        .right-column {
          width: 50%;
          padding: 1.2rem;
          display: flex;
          align-items: center;
          @include for-phone-only {   
            width: 100%; 
          }
        }
        .modal-description {
          font-size: 1.6rem;
          line-height: 1.5;
          color: $white;
        }
      }
    }
  
  
    @include for-phone-only {    
      .modal-content {
        width: 100%;
        height: 100%;
      }
      .modal-columns {
        flex-direction: column;
      }
      .left-column {
        width: 100%;
      }
      .right-column {
        width: 100%;
      }
      .modal-image {
        width: 100%;
      }
    }
  
  
  
  
  }
  
  </style>