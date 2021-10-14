<template>  
    <!-- intro page -->
    <main v-if="page === 0">
      <img src="/onepiece.jpeg" alt="onepiece character">
      <h1>나와 닮은 캐릭착기</h1>
      <h2>나와 닮은 캐릭터는 누굴까?</h2>
      <Button text="테스트시작!" :clickEvent="startTest" />
    </main>
    <!-- quiz page -->
    <main v-else-if="page < 5">
      <Question />
    </main>
    
</template>

<script>
export default {   
    computed: {
      page() {
        return this.$store.state.page;
      },      
    },
    methods: {
      startTest() {
        console.log("startTest");
        this.$store.commit("SET_PAGE", 1);
      }
    }
};
</script>

<style>

</style>
