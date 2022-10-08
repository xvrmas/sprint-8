<template>
    <div>
        <div class="hero">
            <div class="columns has-background-black">
                <div class="column is-two-fifths ">1</div>
                <div class="column  ">
                    <img src="@/assets/starwars-logo.png" alt="logo starwars">
                </div>
                <div class="column has-background-black">
                    <button class="button is-black">LOGIN</button>
                    <button class="button is-black">REGISTER</button>
                </div>
            </div>
            <nav class="navbar" role="navigation" aria-label="main navigation">
                <div class="navbar-brand">
                    <button class="button">HOME</button>
                    <button class="button" @click="showStarShips()">STARSHIPS</button>
                </div>
            </nav>
        </div>
        <PanelStarShips :starShips="starShips"></PanelStarShips>
    </div>
</template>
<script>
import PanelStarShips from '@/components/PanelStarShips.vue';
export default {
    name: "Home",
    components: { PanelStarShips },
    data() {
        return {
            starShips: [],
        }
    },
    methods: {
        async showStarShips() {
            const response = await fetch(`https://swapi.dev/api/starships/`);
            this.starShips = await response.json();
            return this.starShips
        }
    }
}
</script>