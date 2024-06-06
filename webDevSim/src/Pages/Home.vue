<script setup>
import AudioPlusResumeUpload from '../components/audio.vue'
</script>

<script>
import { ref } from 'vue';
import Popup from '../components/submissionPopUp.vue';
export default {
    data () {
        return {
            popupTriggers: {
                buttonTrigger: false
            }
        }
    },
    methods: {
    togglePopup() {
      this.popupTriggers.buttonTrigger = !this.popupTriggers.buttonTrigger;
    },
  },
}

</script>

<template>
    <main>
        <AudioPlusResumeUpload/>
        <button @click="togglePopup">
            <h4>Open Popup</h4>
        </button>
        <Popup v-if="popupTriggers && popupTriggers.buttonTrigger">
            <h2>idk</h2>
        </Popup>
    </main>
</template>
