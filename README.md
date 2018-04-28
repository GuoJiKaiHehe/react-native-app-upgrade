<img src='http://oleeed73x.bkt.clouddn.com/1522417405_153693.png' />

### React Native App 版本升级封装库，兼容Android 4.4+、5.+、6.+、7.+版本

#### Android：
##### （1）版本检测
##### （2）版本下载
##### （3）进度提示
##### （4）下载完成后安装

#### iOS
##### （1）版本检测
##### （2）跳转App Store


#### 


##  使用
   ```
 yarn add https://github.com/puti94/react-native-app-upgrade
 //then
 react-native link react-native-app-upgrade

 //使用xcode将ios_lib下的两个文件添加到项目中
import {upgrade, openAPPStore, addDownListener} from 'react-native-app-upgrade'

if (原生需要升级 && isAndroid) {
    upgrade('apk下载地址')
}

if (isAndroid) {
    addDownListener(progress => console.log('进度', progress + '%'))
}

if (isIOS) {
    upgrade('appid', (msg) => {
        if (msg === 'YES') {
            openAPPStore('APPID')
        }
    })

}

   ```


