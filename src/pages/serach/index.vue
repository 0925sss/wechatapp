<template>
  <div style="width: 100%; height: 100%;">
    <map
      id="map"
      :scale="scale"
      :controls="controls"
      @controltap="controltap($event)"
      :markers="markers"
      :include-points="markers"
      @markertap="markertap($event)"
      show-location
      style="width: 100%; height: 100%;"
    ></map>
  </div>
</template>

<script>
export default {
  data () {
    return {
      type:1,
      scale:16,
      markers: require("@/data/map.json").map((value) => {
        value.label = {}
        value.label.content = value.name
        value.label.color = '#808080'
        value.label.fontSize = 14
        console.log(value)
        return value
        }),
      controls: [{
        id: 1,
        iconPath: '/static/grid/f.png',
        position: {
          left: 10,
          top: 10,
          width: 30,
          height: 30
        },
        clickable: true
      }, {
        id: 2,
        iconPath: '/static/grid/s.png',
        position: {
          left: 10,
          top: 50,
          width: 30,
          height: 30
        },
        clickable: true
      }, {
        id: 3,
        iconPath: '/static/grid/d.png',
        position: {
          left: 10,
          top: 90,
          width: 30,
          height: 30
        },
        clickable: true
      }]
    }
  },

  methods: {
    markertap(event) {
      console.log(event)
    },
    controltap(event) {
      if (event.mp.controlId == 1) {
        this.scale += 1
      } if (event.mp.controlId == 2) {
        this.scale -= 1
      } else {
        this.markers = require("@/data/" + this.type + ".json").map((value) => {
          value.label = {}
          value.label.content = value.name
          value.label.color = '#FF7F00'
          value.label.fontSize = 14
          console.log(value)
          return value
        })
        this.type = this.type + 1;
        if (this.type == 6) this.type = 1
      }
    }
  },

  created () {
  }
}
</script>

<style>
body, html {
  height:100%
}
</style>
