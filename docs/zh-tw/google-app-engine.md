# 佈署ReactJS App到 App Engine

在開始之前 記得先安裝Cloud SDK
裝完後切換到專案目錄下
在 command視窗下 鍵入

`gcloud init`

React 的專案目錄大約如下：

App
|-------- build   ======>這個要build過才有
|-------- node_modules
|-------- public
|-------- src
|-------- .gitignore
|-------- package.json
|-------- package-lock.json

我們需要跟App Engine說 如何去佈署一個service
在根目錄下建立一個  app.yaml 檔案
檔名可以隨意 通常的命名規則為 AppName_ServiceName.yaml

檔案內容大概為：

```js
 #執行環境 standard 只有 'nodejs10' & 'nodejs12' 可以選
  runtime: nodejs10
 
  #每個instance的類別 各類的差別請參考圖2
  instance_class: F2
 
  #這個設定要參考 圖2 的 Supported Scaling Types 來做設定
  #不過大致上可以分 F開頭的 用 automatic scaling
  #B開頭的可以用 manual_scaling & basic_scaling
  #max_instances 可以設定最大的instance數量
  automatic_scaling:
    max_instances: 5
 
  #這裡可以設定如何處理 url pattern
  #App Engine 可以根據不同的 pattern來執行不同的 application
  #當然還有靜態的檔案 ((CSS 圖片 JavaScript之類的
  #我就不解釋這部份了 文件裡面都有寫
  #附上網址  https://cloud.google.com/appengine/docs/standard/nodejs/config/appref?hl=zh_TW
  handlers:
   - url: /
     static_files: build/index.html
     upload: build/index.html
 
   - url: /(.*)
     static_files: build/\1
     upload: build/(.*)
 
  #進入點  可以說是佈署完要啟動的 command
  entrypoint: "npm run remote:start"
```

我們的instance要處理web request 就要有web framework 像是 Express.js Koa.js之類的 都行
不過最快的方法是裝 serve這個套件

```sh
npm install serve
```

接著還記得app.yaml裡的 entrypoint ? 我們在package的scripts加上

```js
 "scripts": {
    ...,
    "remote:start": "serve -s build -l 80",
    ...
  },
```

-l 這個參數是 listening port
build 是我們upload的build 資料夾

.gitignore

```js
.gcloudignore
.git
.gitignore

yarn.lock #刪除
package-lock.json #刪除

node_modules/
src/
public/
```

都處理好後就可以來deploy拉~~
在根目錄下 開啟command line 鍵入

```js
gcloud app deploy
#or
gcloud app deploy 指定的yaml檔
```

執行的過程大概長這樣子

descriptor:      [C:\react\dapp\app.yaml]
source:          [C:\react\dapp]
target project:  [exchange-web-app]
target service:  [default]
target version:  [20201222t150316]
target url:      [https://exchange-web-app.df.r.appspot.com]

> Updating service [default]...failed.
ERROR: (gcloud.app.deploy) Error Response: [7] Access Not Configured. Cloud Build has not been used in project exchange-web-app before or it is disabled. Enable it by visiting https://console.developers.google.com/apis/api/cloudbuild.googleapis.com/overview?project=exchange-web-app then retry. If you enabled this API recently, wait a few minutes for the action to propagate to our systems and retry.

拜訪上述網址 Cloud Build API 啟用計費