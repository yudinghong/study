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
    * M = moveto
    * L = lineto
    * H = horizontal lineto
    * V = vertical lineto
    * C = curveto
    * S = smooth curveto
    * Q = quadratic Bézier curve
    * T = smooth quadratic Bézier curveto
    * A = elliptical Arc
    * Z = closepath
```svg
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
    <path d="M150 0 L75 200 L225 200 Z" />
</svg>
```
<svg width="100" height="100">
    <path d="M15 0 L75 20 L22 20 Z" />
</svg>
