# 移动端适配

#### 使用重点

1. 1rem === 100rpx | 0.01rem === 1rpx | 100vw 就是设备的宽度 等于 750rpx 等于 7.5rem;
2. 使用 rem 是为了作为一个变量载体，承载 css 里面的 vw 单位或者 fontSize.js 里面的 docWidth(屏幕宽度)
3. 0.01rem === 1rpx 举个例子如果设置一个 div 的宽度是 600px/600rpx, 设置 div 的 width 为 6rem

#### 介绍

1. 设置根元素 html 的 font-size;
2. 设置根元素字体大小: 1rem === 100rpx | 0.01rem === 1rpx | 100vw 就是设备的宽度 等于 750rpx 等于 7.5rem;
3. rem 相当于一个载体, rem 根据设备宽度的变化而变化；
4. 类似于微信小程序 rpx。
5. 在 iPhone6 上，屏幕宽度为 375px，共有 750 个物理像素，则 750rpx = 375px = 750 物理像素，1rpx = 0.5px = 1 物理像素。
6. css 中的 px 与设备的物理像素并非绝对的一比一关系。px 与物理像素的比例与设备的 dpr（像素倍率）有关。rpx 称为相对像素值，rpx 与物理像素也并非绝对的一比一关系。
7. wxss 将设备宽定义为 750rpx，是以 iPhone6 的分辨率（750x1334）为基准划分的。
8. 也就是说，在 iPhone6 上，1rpx=1 物理像素=0.5px。
9. 因为设计师标注的尺寸一般是物理分辨率。
10. 所以如果以 iphone6 为标准出设计稿的话，那么我们就可以不需要经过换算直接标准 rpx。

#### 使用说明

1. reset.css 是重置 css 样式标签，引入即可使用。
2. common.css 和 fontSize.js 只需要引入一个即可
3. common.css 引入是用 css 完成移动端适配，兼容性依赖项目对 vw vh 单位的兼容，如果不想导入 js 或者项目兼容 vw vh 单位，建议使用引入 common.css 方法完成适配。
4. fontSize.js 是加载 js 脚本完成移动端适配，原理和 css 方式一样，都是根据设备宽度的变化而变化，他们的区别死兼容性问题，因为 rem 的兼容性比较好，大部分项目都能兼容，设置设置根元素 html 的 font-size 的工作由 fontSize.js 这个脚本执行后完成。
