<template>
    <div>
        <h1
        class="has-text-centered">Home</h1>
        <PanelStarShips></PanelStarShips>
    </div>
</template>
<script>
import PanelStarShips from '@/components/PanelStarShips.vue';
    export default{
    name: "Home",
    components: { PanelStarShips }
}
</script>