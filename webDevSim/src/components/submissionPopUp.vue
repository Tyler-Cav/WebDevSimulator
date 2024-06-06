<template>
    <div class="popup">
        <div class="popup-inner">
            <slot />
            <!-- <p class="submission">
                Thank you for your submission. While your skillset is definitely impressive, we have decided to move forward with another candidate. Or just decided to repost the job next week.
            </p> -->
            <button class="close">
                Close
            </button>
        </div>
    </div>
</template>

<script>
</script>

<style scoped>
.popup {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 99;
    background-color: rgba(0, 0, 0, 0.2);
    display: flex;
    align-items: center;
    justify-content: center;
    color: black;
}

.popup-inner {
    background-color: white;
    padding: 32px;
    border-radius: 20px;
    width: 500px;
}
.submission {
    font-size: large;
}

.close {
    border: 2px solid black;
}

</style>