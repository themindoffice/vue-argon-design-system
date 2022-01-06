<template>
    <div id="app">
        <router-view name="header"></router-view>
        
        <main>
            <slide-x-left-transition origin="center" mode="out-in" :duration="500">
                <router-view/>
            </slide-x-left-transition>
        </main>

        <router-view name="footer"></router-view>
    </div>
</template>

<script>
import { FadeTransition, ZoomCenterTransition, SlideXLeftTransition } from "vue2-transitions";

export default {
  components: {
    FadeTransition,
    ZoomCenterTransition,
    SlideXLeftTransition
  }
};
</script>
