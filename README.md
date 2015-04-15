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

####strokeStyle ,fillStyle e lineWidth
Definem a cor do preenchimento, da borda e espessura da borda do canvas sucessivamente, exemplo:
```javascript
  ctx.fillStyle = "red";
  ctx.strokeStyle = "black";
  ctx.lineWidth = 3;
```

Exemplo usando fill e stroke juntos

```javascript
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>
  <canvas id="mycanvas" width="300" height="300">Your Browser does not support Canvas, please upgrade</canvas>
  <script>
    var canvas = document.getElementById('mycanvas');
    var ctx = canvas.getContext('2d');
    
    ctx.fillStyle = "gray";
    ctx.strokeStyle = "blue";
    ctx.lineWidth = 3;

    ctx.fillRect(50, 50, 100, 100);
    ctx.strokeRect(50, 50, 100, 100);
  </script>
</body>
</html>
```

####Resultado
<img src="img/square.jpg" height="186" width="216" alt="">
