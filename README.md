<p xmlns:cc="http://creativecommons.org/ns#" >Este trabalho está licenciado sob <a href="https://creativecommons.org/licenses/by-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-SA 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""><img style="altura:22px!importante;margem-esquerda:3px;alinhamento-vertical:texto-inferior;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" alt=""></a></p>
let cor;
let circuloX; // horizontal
let circuloY; // vertical

function setup() {
  createCanvas(400, 400); // width x height
  background(color(100,0,0));
  cor = color(random(0,255), random(0,255), random(0,255));
  circuloX = [0,0,0];
  circuloY = [random(height), random(height), random(height)];
}

// circuloX = 0,0,0  
// circuloY = 300, 150 , 150




function draw() {
  
  fill(cor);
  
  //console.log (circuloX.length)
  
  for (let contador in circuloX) {
    // console.log (contador)
  circle(circuloX[contador], circuloY[contador], 50);  
  circuloX[contador] += random (0,3);
  circuloY[contador] += random (-3,3);
    
    if (circuloX[contador] >= width){
      circuloX[contador] = 0;
      circuloY[contador] = random(height);
    }
   
  }
 
  
  
  
  
  if (mouseIsPressed){
    cor = color(random(0,255), random(0,255), random(0,255), random(0,100));
  }
    
}
