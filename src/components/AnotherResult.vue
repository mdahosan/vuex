<template>
    <div>
      <p>Counter is: {{ counter }}</p>
      <p>Number of clicks {{ clicks}}</p>
    </div>
</template>

<script>



    import { mapGetters } from 'vuex'

    export default {
        // props: ['counter']
      // computed: mapGetters([
      //   'doubleCounter', 'stringCounter'
      // ])
      computed: {
        ...mapGetters({
                     counter: 'doubleCounter',
                     clicks: 'stringCounter',
                   })
      }
      // computed: {
      //   counter(){
      //     return this.$store.state.doubleCounter * 2;
      //   },
      //   clicks(){
      //     return this.$store.getters.stringCounter;
      //   }
      // }
    }
</script>
