# Geolocalização
`$ ionic plugin add cordova-plugin-geolocation` 


Repositório:https://github.com/apache/cordova-plugin-geolocation


Este plugin fornece informações sobre a localização do dispositivo, como a latitude e longitude. Fontes comuns de informação de localização incluindo o Sistema de Posicionamento Global (GPS) e localização inferida através de sinal de rede como o Endereço de IP, RFID, WiFi, Bluetooth, endereço de MAC e IDs de células GSM/CDMA. 



Essa API é baseada na especificação da API de Geolocalização do W3C, e somente funciona em dispositivos que ainda não disponibilizam uma implementação.


##Uso

```javascript
import {Geolocation} from 'ionic-native';



Geolocation.getCurrentPosition().then((resp) => {
 //resp.coords.latitude
 //resp.coords.longitude
})

let watch = Geolocation.watchPosition();
watch.subscribe((data) => {
 //data.coords.latitude
 //data.coords.longitude
})
```

##Métodos estáticos

`getCurrentPosition(options)`

Pega a posição atual do dispositivo.

Parametro | Tipo | Detalhes
------------ | ------------- | -------------
Options | `GeolocationOptions` | As opções de geolocalização
