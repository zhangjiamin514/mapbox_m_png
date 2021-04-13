<template>
  <div id='map'>
    <export-map :map=map></export-map>
  </div>
</template>

<script>
import mapboxgl from 'mapbox-gl'
import exportMap from '@/components/export-map/Export'

export default {
  name: 'Map',
  components: {
    exportMap
  },
  data () {
    return {
      map: null
    }
  },
  mounted () {
    this.initMap()
  },
  methods: {
    initMap () {
      let that = this
      let config = that.$baseConfig
      mapboxgl.accessToken = config.accessToken
      let optio = config.mapOp[0]
      let map = new mapboxgl.Map(optio)
      map.addControl(new mapboxgl.NavigationControl(), 'top-left')
      that.map = map
    }
  }
}
</script>

<style scoped>
#map {
  height: 100vh;
  width: 100vw;
}
</style>>
