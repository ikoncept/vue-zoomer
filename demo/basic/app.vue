<template>
    <div style="padding: 100px;">
        <div>
            zoomed: {{ zoomed }}
            <button @click="$refs.zoomer.zoomIn()">
                +
            </button>
            <button @click="$refs.zoomer.zoomOut()">
                -
            </button>
        </div>
        <VZoomer
            ref="zoomer"
            style="width: 500px; height: 500px; border: solid 1px silver;"
            :max-scale="10"
            :zooming-elastic="false"
            :zoomed.sync="zoomed"
            :start-scale="5"
        >
            <img src="../assets/landscape-1.jpg" style="object-fit: contain; width: 100%; height: 100%;">
        </VZoomer>
    </div>
</template>

<script>
export default {
    data () {
        return {
            zoomed: false
        }
    }
}
</script>
