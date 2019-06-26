# miniprogram
小程序资源库

# 在小程序端，如何使用 async/await 语法？
在云函数里，由于 Node 版本最低是 8.9，因此是天然支持 async/await 语法的。而在小程序端则不然。在微信开发者工具里，以及 Android 端手机（浏览器内核是 QQ浏览器的 X5），async/await是天然支持的，但 iOS 端手机在较低版本则不支持，因此需要引入额外的 文件。可把这个 regenerator/runtime.js 文件引用到有使用 async/await 的文件当中。
```
import regeneratorRuntime from '../../utils/runtime.js'
```

