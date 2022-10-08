<template>
    <div>
        <div class="box">
            <PanelInfoShip :infoTechShip="infoTechShip"></PanelInfoShip>
            <div class="field" v-for="(item, index) in starShips.results" :key="index">
                <a class="is-size-5" @click="infoShip(item)">{{item.name.toUpperCase()}}</a>
                <p class="is-size-6">{{item.model}}</p>
            </div>
        </div>
    </div>
</template>
<script>
import PanelInfoShip from '@/components/PanelInfoShip.vue'
export default {
    name: 'PanelStarShips',
    components: { PanelInfoShip },
    props: ["starShips"],
    data() {
        return {
            infoTechShip: []
        }
    },
    methods: {
        infoShip(index) {
            return this.infoTechShip = index
        }
    }
}
</script>
<style>
body {
    background-color: black;
}

h2 {
    padding: 10px;
    border: solid, 1px;
}
</style>