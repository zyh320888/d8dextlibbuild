# d8dcloud.com

用于打包 npm 包


# 初次使用说明

```sh
#运行ncc安装
./initncc.sh
#安装需要打包的npm包，例如 aws-sdk
npm i aws-sdk
```

```js
// /index.js
// require 包
const index = require('aws-sdk');
module.exports = index;
```

```sh
# 运行打包
./build.sh

# 运行结果输出在 /dist/index.js   
# 将/dist/index.js 改名为 aws-sdk.js 
# 放到 d8d后台基座 /extend_modules 下
```

```js
// 到d8dcloud.com IDE 后台服务中import
const aws-sdk = await Import('aws-sdk')
```