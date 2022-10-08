<template>
    <div class="container has-center">
        <h6> Name: '{{infoTechShip.name}} </h6>
        <h6> Model: {{ infoTechShip.model }} </h6>
        <h6> Manufacturer: {{ infoTechShip.manufacturer }}</h6>
        <h6> Passengers: {{ infoTechShip.passengers }} </h6>
        <h6> Crew: {{ infoTechShip.crew }} </h6>
        <h6> StarShip class: {{ infoTechShip.starship_class }} </h6>
        <h6> Cost: {{ infoTechShip.cost_in_credits }} </h6>
    </div>   
</template>
<script>

export default {
    name: 'PanelInfoShip',
    props: ['infoTechShip']
}

</script>