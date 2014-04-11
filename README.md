# SupperWrapper
###description
A module aiming circumvent the limitations using PIL and textwrap concerning these two issues   
- carLim and FontSize optimization when width and height are given   
- draw.text printing outside the expected box

###use
To find the best fontSize and carlim
``` python
import superWrapper
[fontSize,carlim]=optimizeFontSizeAndCarLim(text,fontName,MaxWidth, MaxHeight)#for a multiline
[fontSize,carlim]=ConservativeOptimizeFontSizeNoWrap(text,fontName,MaxWidth, MaxHeight)#for single line
```
To avoid printing outside the box
```python
import superWrapper
correction,size=getTrueMetrics(font,color,text)
x_remaining=w-size[0]
y_remaining=h-size[1]
draw.text((x + x_remaining/2 + correction[0], y+y_remaining/2 + correction[1]), text, fill=color, font=font)
```
###dependancies
- PIL
- ImageEdit

###More
Don't hesitate to fork or/and suggest a better solution.
more informations there http://brunomart.in/blog/?p=14

