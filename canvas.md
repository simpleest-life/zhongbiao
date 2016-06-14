# canvas常用API


## 矩形
* ctx.fillRect(x,y,width,height)    填充矩形
* ctx.strokeRext(x,y,width,height)  框线矩形


## 圆
* ctx.arc(x,y,r,start,end,true)         圆
* ctx.arcTo()       圆弧


## 线
* ctx.beginPath()   开始一个路径
* ctx.moveTo(x,y)      移动画笔到某点
* ctx.lineTo(x,y)      让路径中拥有一条到某点的线   并不会直接绘出
* ctx.rect(x,y,width,height)     让路径中拥有矩形   并不会直接绘出
* ctx.fill()        填充当前路径
* ctx.stroke()      描边当前路径
* ctx.closePath()   结束一个路径

* ctx.quadraticCurveTo(cplx,cplx,x,y)  二次贝塞尔曲线
* ctx.bezierCurveTo(cplx,cplx,cp2x,cp2y,x,y)  三次贝塞尔曲线


从画布中清除矩形区域
画布的特点，绘制上元素无法更改
* ctx.clearRect();   eg:document.onclick=function(){ctx.clearRext(0,0,600,600)}  0,0+画布的原宽高
                        canvas.with=canvs.height=600;  画布的原宽高

## 样式
* ctx.fillStyle="rgba()"
* ctx.strokeStyle='#fff'
* ctx.globalAlpha=0.2;  全局透明度
* ctx.lineWidth
* ctx.lineCap
* ctx.lineJoin
* ctx.miterlimit
* ctx.getLineDash()
* ctx.setLineDash()
* ctx.lineDashffset

* ctx.create


## 画布中的位移旋转和变形(挪动画布)  只保存画布状态
* ctx.save()
* ctx.restore()
* ctx.translate()
* ctx.rotate((Math.PI/180))