<script setup>
import AudioPlusResumeUpload from '../components/audio.vue'
</script>

<script>
import { ref } from 'vue';
import Popup from '../components/submissionPopUp.vue';
export default {
    setup () {
        let popupTriggers = ref({
            buttonTrigger: true
        });
        return {
            Popup,
            popupTriggers,
         }
    }
}

</script>

<template>
    <main>
        <AudioPlusResumeUpload/>
        <button>
            <h4>Open Popup</h4>
        </button>
        <Popup v-if="popupTriggers.buttonTrigger">
            <h2>idk</h2>
        </Popup>
    </main>
</template>
