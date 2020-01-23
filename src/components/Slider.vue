<template>
<div class="slider-block">
    <input type="range" 
    max="1000"
    min="0"
    v-model="itemSkill"
    class="slider"
    />
</div>
</template>

<script>
export default {
    data: () =>({
        itemSkill: "485"
    }),
}
</script>