# 关于 Fresco 中文版

Fresco是一个强大的系统用于在Android应用中展示图片，它能够从网络、本地存储和本地资源中加载图片。它拥有三级缓存,Fresco在显示方面是用了Drawees，可以显示占位符，直到图片加载完成。

本教程内容来源于 [fresco 中文网](http://fresco-cn.org/)

英文官网Fresco：<http://frescolib.org/>

|更新日期    |更新内容
|----------|--------------------
|2015-04-01|Fresco 中文版发布

Fresco 是一个强大的系统用于在 Android 应用中展示图片，它能够从网络、本地存储和本地资源中加载图片。它拥有三级缓存，Fresco 在显示方面是用了 Drawees，可以显示占位符，直到图片加载完成。

Fresco 是一个强大的图片加载组件。

Fresco 中设计有一个叫做 image pipeline 的模块。它负责从网络，从本地文件系统，本地资源加载图片。为了最大限度节省空间和 CPU 时间，它含有 3 级缓存设计（2 级内存，1 级文件）。

Fresco 中设计有一个叫做 Drawees 模块，方便地显示 loading 图，当图片不再显示在屏幕上时，及时地释放内存和空间占用。

Fresco 支持 Android2.3(API level 9) 及其以上系统。

## 特性

### 内存管理

一个没有未压缩的图片，即 Android 中的 Bitmap，占用大量的内存。大的内存占用势必引发更加频繁的 GC。在 5.0 以下，GC 将会显著地引发界面卡顿。

在 5.0 以下系统，Fresco 将图片放到一个特别的内存区域。当然，在图片不显示的时候，占用的内存会自动被释放。这会使得 APP 更加流畅，减少因图片内存占用而引发的 OOM。

Fresco 在低端机器上表现一样出色，你再也不用因图片内存占用而思前想后。

### 图片的渐进式呈现

渐进式的 JPEG 图片格式已经流行数年了，渐进式图片格式先呈现大致的图片轮廓，然后随着图片下载的继续，呈现逐渐清晰的图片，这对于移动设备，尤其是慢网络有极大的利好，可带来更好的用户体验。

Android 本身的图片库不支持此格式，但是 Fresco 支持。使用时，和往常一样，仅仅需要提供一个图片的 URI 即可，剩下的事情，Fresco 会处理。

### Gif 图和 WebP 格式

是的，支持加载 Gif 图，支持 WebP 格式。

#### 图像的呈现

Fresco 的 Drawees 设计，带来一些有用的特性：

- 自定义居中焦点(对人脸等图片显示非常有帮助)
- 圆角图，当然圆圈也行。
- 下载失败之后，点击重现下载
- 自定义占位图，自定义overlay, 或者进度条
- 指定用户按压时的overlay

#### 图像的加载

Fresco 的 image pipeline 设计，允许用户在多方面控制图片的加载：

- 为同一个图片指定不同的远程路径，或者使用已经存在本地缓存中的图片
- 先显示一个低解析度的图片，等高清图下载完之后再显示高清图
- 加载完成回调通知
- 对于本地图，如有EXIF缩略图，在大图加载完成之前，可先显示缩略图
- 缩放或者旋转图片
- 处理已下载的图片
- WebP 支持

>
本教程内容来源于：<http://fresco-cn.org>   
Fresco 官网：<http://frescolib.org/>

|更新日期    |更新内容
|----------|--------------------
|2015-04-08|Fresco 中文版发布



