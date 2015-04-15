#LAB de testes com Canvas

##Proprieadades principais até o momento

##Início
>#####Antes de tudo deve-se criar uma tag <canvas\> no HTML e esta deve conter inicialmente um width="" e um height="" mesmo que estas propriedades sejam alteradas futuramente, também é interessante colocar alguma mensagem ou imagem dentro da tag canvas para agir como um Fallback caso o browser não suporte o uso de canvas, exemplo:

```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
  	<meta charset="UTF-8">
  	<title>Document</title>
  </head>
  <body>
  	<canvas id="mycanvas" width="WIDTH" height="HEIGHT">
  	  Your Browser does not support Canvas, please upgrade
  	</canvas>
  </body>
  </html>
```

---------------------------------------------

###Referenciando Canvas e Pegando seu Contexto
#####Recuperando a tag canvas em uma variavel
```javascript
var canvas = document.getElementById('mycanvas');
```

#####Pegando o contexto do canvas
```javascript
var ctx = canvas.getContext('2d');
```

-----------------------------------------------

###Retângulo


####fillRect(x , y, width, height );

Um retângulo preenchido com o posicionamento baseado em x,y e medidas de width, height

-----------------------------------------------
####strokeRect(x, y, width, height);
Um retângulo somente borda com o posicionamento baseado em x,y e medidas de width, height

-----------------------------------------------

####strokeStyle e fillStyle
Definem a cor do preenchimento e da borda do canvas sucessivamente, exemplo:
```javascript
  ctx.fillStyle = "red";
  ctx.strokeStyle = "black";
```