# UnityforBlur
For using UGUI Blur 
实现原理，通过两个摄像机，Main摄像机来补抓的是游戏画面,第二个摄像机主要通过渲染RawImage，第一帧的画面进行补抓
然后通过RawImage的图像进行采样
一个均值模糊shader来赋值在Rawimage中
通过gameObject.enable来控制渲染开始
在OnImageRenderer() 方法里面 在画面渲染完成后的第一帧补抓 然后立刻enable=false 停止补抓
该方法在目前升级管线之后的URP 无法使用 版本为2020,1.3F
![732729](https://user-images.githubusercontent.com/65991081/111276934-da317480-8672-11eb-99a6-de0dd09785d3.jpg)
