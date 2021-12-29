<template>
  <l-map class="map_style" style="height: 500px" :zoom="zoom" :center="center">
    <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
    <l-marker :lat-lng="markerLatLng">
      <l-tooltip :options="{ permanent: true, interactive: true }">
        <div class="popup__title">Playroom Kids Club Київ</div>
        <div class="popup__row">
          <div class="popup__row__adress">пров. Чеховський,3 <br> <span>( лише гурткова діяльність)</span></div>
          <div class="popup__row__tel">Телефон: <a href="tel:066 937 24 24">066 937 24 24</a></div>
        </div>
        <div class="popup__row" style="margin-top: 30px;">
          <div class="popup__row__adress">вул. Бульварно-Кудрявська, 45<br><span>( садочок для дітей від 2-6 років)</span></div>
          <div class="popup__row__tel">Телефон: <a href="tel:095 738 52 48">095 738 52 48</a></div>
        </div>
      </l-tooltip>
    </l-marker>
  </l-map>
</template>

<script>
import {LMap, LTileLayer, LMarker, LTooltip} from 'vue2-leaflet';
import { Icon } from 'leaflet';

delete Icon.Default.prototype._getIconUrl;
Icon.Default.mergeOptions({
  iconRetinaUrl: require('leaflet/dist/images/marker-icon-2x.png'),
  iconUrl: require('leaflet/dist/images/marker-icon.png'),
  shadowUrl: require('leaflet/dist/images/marker-shadow.png'),
});

export default {
  name: "Map_kyiev",
  components: {
    LMap,
    LTileLayer,
    LMarker,
    LTooltip
  },
  data () {
    return {
      url: 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
      zoom: 15,
      center: [50.4505914, 30.5000608],
      markerLatLng: [50.4505914, 30.5000608],
    };
  }
}
</script>

<style>
.popup__title{
  font-weight: 800;
  font-size: 30px;
  color: #7DD3CA;
  text-align: center;
}
.popup__row__adress{
  font-weight: normal;
  font-size: 20px;
  color: #BEA32E;
}
.popup__row__adress span {
  color: black;
}
.popup__row__tel{
  font-weight: normal;
  font-size: 20px;
  color: black;
}
.popup__row__tel a{
  text-decoration: none;
  color: #BEA32E !important;
}
@media screen and (max-width: 375px) {
  .map_style{
    height:500px !important;
  }
  .leaflet-tooltip{
    transform: translate3d(10px, 268px, 0px) !important;
    width: 310px !important;
  }
  .popup__title{
    font-size: 19px;
  }
  .popup__row__adress{
    font-size: 20px;
  }
  .popup__row__adress span{
    font-size: 15px;
  }
}

</style>