<template>
  <div>
    <bottom-scroll @on-bottom="onBottom">
      <div v-for="id in content" :key="id">
        <img :src="'https://picsum.photos/200/300?r=' + id"/>
      </div>
    </bottom-scroll>
  </div>
</template>
<script>
import BottomScroll from './bottom-scroll'
export default {
  components: {
    BottomScroll
  },
  created () {
    for (let i=0; i<10; i++) {
      this.content.push(i);
    }
  },
  data () {
    return {
      content: []
    }
  },
  methods: {
    onBottom () {
      console.log('On bottom reached ! Fetch next 3 pics')
      let len = this.content.length;
      for (let i=len; i<len + 3; i++) {
        this.content.push(i)
      }

    }
  }
}
</script>
