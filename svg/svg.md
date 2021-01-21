# SVG
[toc]

## SVG file
```svg
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
  <circle cx="100" cy="50" r="40" stroke="black"
  stroke-width="2" fill="red" />
</svg>
```

## rect
* properties
    * width 
    * height
    * stroke
    * stroke-width (边框会内外各扩一半宽度,额外绘制)
    * fill (none: 透明)
    * x
    * y
    * fill-opacity
    * stroke-opacity
    * opacity
    * rx
    * ry 
```svg
<svg width="100" height="100">
    <rect width="60" height="60" x="10" y="10" stroke-width="4" stroke="red" rx="2" ry="18" />
</svg>
```
<svg width="100" height="100">
    <rect width="60" height="60" x="10" y="10" stroke-width="4" stroke="red" rx="2" ry="18" />
</svg>

## circle
* properties
    * cx
    * cy
    * r
    * 线类型同上
```svg
<svg width="100" height="100">
    <circle cx="20" cy="20" r="10" stroke-width="4" stroke="red" />
</svg>
```
<svg width="100" height="100">
    <circle cx="20" cy="20" r="10" stroke-width="4" stroke="red" />
</svg>

## ellipse
* properties
    * cx
    * cy
    * rx
    * ry
    * 线类型同上
```svg
<svg width="100" height="100">
    <ellipse cx="30" cy="30" rx="14" ry="8" stroke="red" stroke-width="4" />
</svg>
```
<svg width="100" height="100">
    <ellipse cx="30" cy="30" rx="14" ry="8" stroke="red" stroke-width="4" />
</svg>

## line
* properties
    * x1
    * y1
    * x2
    * y2
```svg
<svg width="100" height="100">
    <line x1="10" y1="10" x2="60" y2="20" stroke-width="4" stroke="red" />
</svg>
```
<svg width="100" height="100">
    <line x1="10" y1="10" x2="60" y2="20" stroke-width="4" stroke="red" />
</svg>

## polygon
* properties
    * points (points="x,x x,x x,x")
    *  fill-rule (nonzero, evenodd)
```svg
<svg width="100" height="100">
    <polygon points="10,10 20,20 30,70 10,30" stroke="red" stroke-width="4"></polygon>
</svg>
```
<svg width="100" height="100">
    <polygon points="10,10 20,20 30,70 10,30" stroke="red" stroke-width="4" ></polygon>
</svg>

### fill-rule
> **nonzero**
> 字面意思是“非零”。按该规则，要判断一个点是否在图形内，从该点作任意方向的一条射线，然后检测射线与图形路径的交点情况。从0开始计数，路径从左向右穿过射线则计数加1，从右向左穿过射线则计数减1。得出计数结果后，如果结果是0，则认为点在图形外部，否则认为在内部。

> **evenodd**
> 字面意思是“奇偶”。按该规则，要判断一个点是否在图形内，从该点作任意方向的一条射线，然后检测射线与图形路径的交点的数量。如果结果是奇数则认为点在内部，是偶数则认为点在外部。

## polyline
* properties
    * points (points="x,x x,x x,x")
```svg
<svg width="100" height="100">
    <polyline points="20,20 40,25 30,30 80,70" stroke="red" fill="none" stroke-width="4" />
</svg>
```
<svg width="100" height="100">
    <polyline points="20,20 40,25 30,30 80,70" stroke="red" fill="none" stroke-width="4" />
</svg>

## path
* properties
    * M = moveto (x y)
    * L = lineto 
    * H = horizontal lineto (H x | h dx)
    * V = vertical lineto (V y | v dy)
    * C = curveto (C x1 y1, x2 y2, x y | c dx1 dy1, dx2 dy2, dx dy)
    * S = smooth curveto
    * Q = quadratic Bézier curve (Q x1 y1, x y | q dx1 dy1, dx dy)
    * T = smooth quadratic Bézier curveto
    * A = elliptical Arc (rx ry x-axis-rotation[1大弧 0小弧] large-arc-flag[1顺 0逆] x y)
    * Z = closepath
```svg
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
    <path d="M150 0 L75 200 L225 200 Z" />
</svg>
```
<svg width="100" height="100">
    <path d="M15 0 L75 20 L22 20 Z" />
</svg>

## text
* properties 
    * transform 
```svg
<svg>
    <text x="10" y="10" fill="red" transform="rotate(90 10,10)">it's a test string</text>
</svg>
```
<svg>
    <text x="10" y="10" fill="red" transform="rotate(20 10,10)">it's a test string</text>
</svg>

```svg
<svg>
    <defs>
        <path id="myPath" d="M10 10 Q 80 80 240 10" /> 
    </defs>
    <use xlink:href="#myPath" fill="none" stroke="red"  />
    <text fill="red" font-size="30">
        <textPath xlink:href="#myPath" >it's a test string</textPath>
    </text>
</svg>
```
<svg>
    <defs>
        <path id="myPath" d="M10 10 Q 80 80 240 10" /> 
    </defs>
    <use xlink:href="#myPath" fill="none" stroke="red"  />
    <text fill="red" font-size="30">
        <textPath xlink:href="#myPath" >it's a test string</textPath>
    </text>
</svg>

> 1. 坐标系的x轴为path；
> 2. 坐标系的y轴在x轴的任意点上，方向都不一致，但是必然是该点对于x轴切线的垂直线。

## stroke
* properties 
    * stroke
    * stroke-width
    * stroke-linecap (butt round square)
    * stroke-dasharray (len offset)   len offset len offset ... 
    * stroke-dashoffset
```svg
<svg>
   <line x1="10" y1="10" x2="140" y2="10" stroke="red" stroke-width="4" stroke-dasharray="10 3" /> 
   <line x1="10" y1="20" x2="140" y2="20" stroke="red" stroke-width="4" stroke-dasharray="10 3 5" />
</svg>
```
<svg>
   <line x1="10" y1="10" x2="140" y2="10" stroke="red" stroke-width="4" stroke-dasharray="10 3" /> 
   <line x1="10" y1="20" x2="140" y2="20" stroke="red" stroke-width="4" stroke-dasharray="10 3 5" />
</svg>

## Filter 
* feBlend - 与图像相结合的滤镜
* feColorMatrix - 用于彩色滤光片转换
* feComponentTransfer
* feComposite
* feConvolveMatrix
* feDiffuseLighting
* feDisplacementMap
* feFlood
* feGaussianBlur
* feImage
* feMerge
* feMorphology
* feOffset - 过滤阴影
* feSpecularLighting
* feTile
* feTurbulence
* feDistantLight - 用于照明过滤
* fePointLight - 用于照明过滤
* feSpotLight - 用于照明过滤
```svg
<svg>
  <defs>
    <filter id="f1" x="0" y="0">
      <feGaussianBlur in="SourceGraphic" stdDeviation="15" />
    </filter>
  </defs>
  <rect width="90" height="90" stroke="green" stroke-width="3"
  fill="yellow" filter="url(#f1)" />
</svg>
```
<svg>
  <defs>
    <filter id="f1" x="0" y="0">
      <feGaussianBlur in="SourceGraphic" stdDeviation="15" />
    </filter>
  </defs>
  <rect width="90" height="90" stroke="green" stroke-width="3"
  fill="yellow" filter="url(#f1)" />
</svg>

[阴影](https://www.runoob.com/svg/svg-feoffset.html)
[渐变-线性](https://www.runoob.com/svg/svg-grad-linear.html)
[渐变-放射性](https://www.runoob.com/svg/svg-grad-radial.html)
