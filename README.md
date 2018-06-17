# Canvas gauges

Canvas gauges 2 component is based on https://www.npmjs.com/package/vue-canvas-gauges but it add watch over options and it is compatible with vue2!

## Installation

```
$ yarn add vue2-canvas-gauges --save
```

## Examples

```vue
<div>
  <linear-gauge :value="value" :options="options"></linear-gauge>
</div>

<script>
  import LinearGauge from 'vue2-canvas-gauges/src/LinearGauge'
  import RadialGauge from 'vue2-canvas-gauges/src/RadialGauge'

  export default {
    components: {
      LinearGauge,
      RadialGauge
    },
    props: {
      value: {
        type: Number,
        default: 50
      },
      title: {
        type: String,
        default: ''
      },
      options: { // https://canvas-gauges.com/documentation/user-guide/configuration
        type: Object,
        default: () => ({
          units: '°C',
          title: 'title',
          minValue: 0,
          maxValue: 300,
          width: 80,
          height: 200,
          strokeTicks: true,
          colorBar: 'white',
          colorBarProgress: 'blue',
          highlights: [ {
            'from': 100,
            'to': 220,
            'color': 'red'
          }
          ],
          minorTicks: 10,
          majorTicks: [
            '0',
            '20',
            '40',
            '60',
            '80',
            '100',
            '120',
            '140',
            '160',
            '180',
            '200',
            '220'
          ],
          colorPlate: '#fff',
          borderShadowWidth: 0,
          borders: false,
          needleType: 'arrow',
          needleShadow: true,
          needleWidth: 0,
          needleCircleSize: 7,
          needleCircleOuter: true,
          needleCircleInner: false,
          numberSide: 'left',
          needleSide: 'left',
          animationDuration: 1500,
          animationRule: 'bounce',
          barWidth: 15,
          valueBox: true,
          valueBoxStroke: 5,
          valueTextShadow: true,
          valueDec: 1,
          barBeginCircle: 0,
          fontNumbersSize: 28,
          fontUnitsSize: 30,
          fontValueSize: 30
        })
      }
    }
  }
</script>


```


## Badges

![](https://img.shields.io/badge/license-MIT-blue.svg)
![](https://img.shields.io/badge/status-stable-green.svg)

---

> GitHub [@cpfarher](https://github.com/cpfarher) &nbsp;&middot;&nbsp;
> Twitter [@cfarerr](https://twitter.com/cfarerr)
