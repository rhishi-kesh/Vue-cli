<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-7 mt-5 text-center">
                <h5>About Page</h5>
                <button @click="display=!display">Click</button>
                <Transition 
                    name="appear"
                    enter-active-class="animate__animated animate__tada"
                    leave-active-class="animate__animated animate__jello"
                >
                    <div class="shadow mt-3" v-if="display">
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. A perspiciatis temporibus culpa maiores placeat labore, ab consequuntur, dicta explicabo recusandae quos, expedita nobis quae facere sapiente reiciendis harum vero iusto? Similique minima eveniet odio deserunt harum, sed quibusdam vero perferendis.</p>
                    </div>
                </Transition>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return{
                display: false
            }
        }
    }
</script>
<!-- 
<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
/*
  Enter and leave animations can use different
  durations and timing functions.
*/
.slide-fade-enter-active {
    transition: all 0.3s ease-out;
  }
  
  .slide-fade-leave-active {
    transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
  }
  
  .slide-fade-enter-from,
  .slide-fade-leave-to {
    transform: translateX(20px);
    opacity: 0;
  }
</style> -->