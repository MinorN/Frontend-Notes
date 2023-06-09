# HTML-03——图片

如果一个页面上有大量的图片，那么势必会导致一个问题：加载很慢，那么该如何优化呢？

1. 最长常见的方法肯定就是图片的懒加载：也就是判断图片当前位置是否在用户课件区域，在就优先加载
2. **预加载**：也就是在页面加载过程中，提前加载图片资源
3. 压缩图片的大小
4. 使用一些特殊编码的图片：比如一些较小的图标可以直接使用 `base64`

这里其实面试的时候，可能会问道：什么使用使用链接获取远程图片地址？什么时候用base64？有什么区别？

* 使用链接获取图片地址：适用于图片文件较大，且需要频繁更新的情况，例如需要从服务器动态加载图片的应用。此时，将图片嵌入到HTML或CSS中，会增加HTML或CSS文件的大小，影响页面的加载速度。而使用链接获取图片地址，则可以将图片文件存储在远程服务器上，减轻前端的负担，同时也方便进行图片更新和管理。
* 使用base64嵌入图片：适用于图片文件较小，且不需要频繁更新的情况，例如icon图标、背景图等。使用base64编码可以减少HTTP请求，从而提高页面的加载速度。此外，还可以在CSS中直接使用base64编码，从而避免HTTP请求，进一步提高页面性能。但是，由于base64编码会使图片数据变大，因此不适用于大型图片。

所以，如果一般需要加载的图片较大、图片需要动态加载——链接获取图片地址；如果图片文件较小、不需要频繁更新——base64编码