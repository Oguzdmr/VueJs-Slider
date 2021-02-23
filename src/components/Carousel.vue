<template>
  <div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="8000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
    >

      <b-carousel-slide v-for="newElement in news" :key="newElement.img" 
        :caption=newElement.title
        :text=newElement.content>

        <template #img>
          <img
            class="d-block img-fluid w-100"
            :src= newElement.img
            width="1024"
            height="480"
          >
        </template>
      </b-carousel-slide> 
    </b-carousel>

    <p class="mt-4">
      Slide #: {{ slide }}<br>
    </p>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        slide: 0,
        sliding: null,
        news: [
          {img: 'https://picsum.photos/1024/480/?image=50', title: 'BIRINCI', content: 'Vue Güzeldir'},
          {img: 'https://picsum.photos/1024/480/?image=51', title: 'IKINCI', content: 'Python Güzeldir'},
          {img: 'https://picsum.photos/1024/480/?image=52', title: 'UCUNCU', content: 'React Güzeldir'},
          {img: 'https://picsum.photos/1024/480/?image=53', title: 'DORDUNCU', content:'Django Güzeldir'},
          {img: 'https://picsum.photos/1024/480/?image=54', title: 'BESINCI', content: 'Flask Güzeldir'},
          {img: 'https://picsum.photos/1024/480/?image=55', title: 'ALTINCI', content: '.NET Güzeldir'},
          {img: 'https://picsum.photos/1024/480/?image=56', title: 'YEDINCI', content:'Git Güzeldir'},
          {img: 'https://picsum.photos/1024/480/?image=57', title: 'SEKIZINCI', content: 'Selenium Güzeldir'},
        ],
      }
    },
    methods: {
      
    }
  }
</script>