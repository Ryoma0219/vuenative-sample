<template>
  <view class="container">
    <text>
      {{ myMessage }}
    </text>
    <touchable-opacity class="button" :on-press="sayHello">
      <text class="button-text">ボタン</text>
    </touchable-opacity>
    <!-- <image :source="image" /> -->
  </view>
</template>
 
 <script>
  // import { RNCamera } from 'react-native-camera';
  // import { Camera, Permissions } from 'expo';
  // import { Toast } from 'native-base';

  export default {
    data() {
      return {
        myMessage: 'こんにちは！',
        hasCameraPermission: false,
        // type: Camera.Constants.Type.back,
        image: {
          uri: ''
        }
      }
    },
    methods: {
      sayHello() {
        alert('Hello, World !');
        this.myMessage = '文字を変えてみた';
      },
      takePhoto() {
        this.launchCamera();
      },
      launchCamera() {
        // console.log(this.RNCamera);
        // this.RNCamera.takePictureAsync()
        //   .then(data => {
        //     Toast.show({
        //       text: 'Success',
        //       buttonText: 'Okay',
        //       duration: 2000,
        //     });
        //     this.image.uri = pictureData.url;
        //   });
      }
    },
    mounted() {
      // Permissions.askAsync(Permissions.CAMERA)
      //   .then(status => {
      //     hasCameraPermission = status.status == "granted" ? true : false;
      //   }).catch((err) => {
      //       console.log(err);
      //   });
    }
    // components: { RNCamera, Camera },
  }
 
 </script>
<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
  font-size: 10px;
}
.button {
  background-color: #3358d3;
  padding: 12px 48px;
  border-radius: 4px;
  margin-top: 12px;
}
.button-text {
  font-size: 18px;
  color: #ffffff;
}
</style>
