
# Configurando ambiente de desenvolvimento mobile (Android)

## Android Studio
Baixe o Android Studio:
  [https://developer.android.com/studio](https://developer.android.com/studio)

Após a instalação, [crie um emulador](https://developer.android.com/studio/run/managing-avds.html?hl=pt-br) através do AVD Manager do Android Studio `tools > AVD Manager`  (na aba x86 selecione algum que seja **x86, x64**)

## Variáveis de ambiente

Procure pelo SDK do Android. Se a instação do Android Studio foi padrão. provavelmente o caminho do SDK será: `C:\Users\USERNAME\AppData\Local\Android\Sdk
`

Após localizar o caminho do SDK, inclua o caminho das seguintes pastas nas **variáveis de ambiente** do seu computador:

 1. `.../platform-tools`
 2. `.../emulator`

### Emulador
Para abrir o emulador sem abrir o Android Studio, execute o comando:
`emulator -avd nome_do_emulador` (Lembrando que o nome do emulador você configura no Android Studio, no momento de criação do mesmo)

Caso não se lembre do nome que colocou, rode o comando `emulator -list-avds`


## Instalação

Você precisará instalar: 

 1. [Node
](https://nodejs.org/)
 2. [Yarn](https://yarnpkg.com/pt-BR/)
 3. [React Native CLI](https://facebook.github.io/react-native/docs/getting-started.html) (`npm install -g react-native-cli`)

Na pasta do projeto execute o comando:
`yarn`

Dentro do diretório `/android` crie um arquivo com o nome `local.properties` com as seguintes informações:
`sdk.dir = C:/Users/USER_NAME/AppData/Local/Android/Sdk`

Abra o terminal e execute o comando:
`yarn start` ou `react-native start --port=8088 --reset-cache`

Em outra aba do terminal, execute o comando: 
`yarn android` ou `react-native run-android`



## Reactotron

Pra conseguir utilizar o [Reactotron](https://github.com/infinitered/reactotron), execute o seguinte comando:
`adb reverse tcp:9090 tcp:9090`



## Gerar APK
Pra gerar um APK do seu aplicativo eu recomendo o seguinte tutorial:
[https://tableless.com.br/react-native-build-release-android/](https://tableless.com.br/react-native-build-release-android/)

## Instalar APK no emulador
Para intalar qualquer APK no emulador, execute o seguinte comando:
`adb install camino_do_apk/nome_do_apk.apk`
