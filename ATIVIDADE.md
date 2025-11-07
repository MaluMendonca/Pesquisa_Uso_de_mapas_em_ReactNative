# <div align="center"> <a href="https://git.io/typing-svg"> <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=22&pause=10000000000&color=FFBFEF&center=true&vCenter=true&random=false&width=524&lines=%E2%8A%B9+Minha+pesquisa!+%E2%8A%B9+" alt="Typing SVG"> </a> </div><img align="center" alt="" src="./src/header-gif.gif">

<h3 align="center" >1. INTRODUÇÃO </h3>


O react-native-maps é uma biblioteca popular para integração de mapas em aplicações React Native. Desenvolvida pela comunidade e com suporte do Expo, ela permite a exibição de mapas interativos utilizando Google Maps no Android e Apple Maps ou Google Maps no iOS!

# <h3 align="center" >2. INSTALAÇÃO E CONFIGURAÇÃO</h3>


Para projetos Expo, a instalação é simples:

bash:
-      npx expo install react-native-maps
  
É necessário configurar as permissões de localização no arquivo app.json: <br>
json:
-      {
        "expo": {
        "plugins": [
        ["expo-location", {
        "locationAlwaysAndWhenInUsePermission": "Permitir o app usar sua localização."
            }]
          ]
         }
      }

# <h3 align="center" >3. IMPLEMENTAÇÃO BÁSICA</h3>


O código básico para exibir um mapa consiste em:

jsx:
-      import MapView from 'react-native-maps';

      <MapView
      style={styles.map}
      initialRegion={{
      latitude: -23.5505,
      longitude: -46.6333,
      latitudeDelta: 0.0922,
      longitudeDelta: 0.0421,
      }}
      showsUserLocation={true}
      />

# <h3 align="center" >4. PRINCIPAIS COMPONENTES E FUNCIONALIDADES</h3>

<h3 align="center" >4.1 MapView: Componente principal para exibir o mapa
</h3>

-      initialRegion: Define a região inicial

-      showsUserLocation: Mostra a localização do usuário

-      zoomEnabled: Permite zoom

-      scrollEnabled: Permite arrastar o mapa

# <h3 align="center" >4.2 Marker: Para adicionar marcadores</h3>


  jsx:
-      <Marker
      coordinate={{latitude: -23.5505, longitude: -46.6333}}
      title="Localização"
      description="Descrição do local"
      />


# <h3 align="center" >4.3 INTEGRAÇÃO COM LOCALIZAÇÃO</h3>

Para capturar a localização do usuário e centralizar o mapa:

jsx:
-      import * as Location from 'expo-location';

      // Solicitar permissão
      const { status } = await Location.requestForegroundPermissionsAsync();

      // Obter localização
      const location = await Location.getCurrentPositionAsync({});



# <h3 align="center" >5. CONCLUSÃO </h3>
O react-native-maps é uma solução robusta e bem documentada para implementação de mapas em React Native. Sua integração com expo-location permite criar aplicativos com funcionalidades de geolocalização de forma eficiente, desde mapas simples até aplicações mais complexas com múltiplos marcadores e rotas!
