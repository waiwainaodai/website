### 使用须知

不同于市面上的建群类软件，此开源代码仅仅用于社群分流。

---

#### Demo

网址 https://shaperword.github.io/website/

PC访问可以看到大概，该设计仅为移动端的微信长按扫码使用，可将该网址复制到微信打开。

这里采用的是分流的办法，即提前准备好若干微信群的二维码，通过一个总的二维码扫描进入网站，网站随机显示群二维码提供自动加群分流功能，每个群上限100人。

---

#### 二维码图片存放

img文件夹中用来存放已经建好的群的二维码，格式统一为：test+数字.png，如“test1.png”"test2.png"，这里的截图建议使用QQ截图截取微信群的二维码部分（其余文字部分都不截取）。



举例：这是微信群二维码的截图。![](https://github.com/shaperword/website/blob/master/img/test1.png)

---

#### 网页相关设置

index.html文件中包含了`<title></title>`字样，中间内容为“景略集智直播系列”，将该部分文字替换即可替换相应网页的标题。

在`<div id="word">`部分中有一个`<p></p>`格式的内容，中间的文字为网页内容部分的标题，建议替换为相应公司的名字。

在`<div id="subword">`部分中有一个`<p></p>`格式的内容，中间的文字部分为“长按识别二维码进群”，建议保留不变。

---



#### 随机显示二维码

使用了一个random（）函数，随机生成0-9个数，随机加载1-10个群，这里默认的是加载png格式的二维码，如有需要可以更换为jpg。

---

#### 使用方法

在github上点击fork按钮，fork该repository到自己账户，进入该仓库，点击settings设置，在Github Pages里选择master branch，点击save。

完成后会显示Your site is published at XXXXXXXXXXXX。（一个网址）。

复制该网址，用草料二维码或者联图二维码根据网址生成二维码，这个二维码就是海报上的二维码入口。

git clone该repository到本地。

建立10个微信群，截图每个二维码，并按照test1.png这样的方式依次命名，替换掉img里相同名字的文件。

改写index.html里的中文标题等内容。

git push该repo到github上。





