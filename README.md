# element-chunk-upload
# 一个基于element-upload改造之后的大文件分片上传组件Demo

 把项目拷贝下来
```
npm install
```
之后

```
npm run serve
```

新增了2个参数
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|---------- |-------------- |---------- |--------------------------------------  |-------- |
| chunk-size| 每块切片的大小，单位 B，如 5MB 需要写成 1024\*1024\*5| Number | — | 1024\*1024\*10 |
| thread| 线程，允许同一时间上传的分片数量| Number | — | 3 |

修改了一个参数
| 参数 | 说明 | 类型 | 可选值 | 默认值 |
|---------- |-------------- |---------- |--------------------------------------  |-------- |
| data| 此方法要返回一个对象，这个对象内容就是每个分片携带的额外参数，参数option是一个对象，里面有chunkSize（当前分片的大小），chunkTotal（分片总数），chunkIndex（分片下标），chunkHash（分片hash），fileName（文件名），fileHash（文件hash），fileSize（文件大小）七个属性 | function(options)| — | — |

其他用法与[element-upload](https://element.eleme.cn/#/zh-CN/component/upload)一致

直接把src/components/upload整个文件夹拷走就能用了
记得要安装
```
npm i spark-md5
```