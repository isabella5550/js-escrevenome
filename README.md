# js-escrevenome
//variaveis da bolinha 
let xbolinha = 100;
let ybolinha = 200;
let diametro = 20;
let raio = diametro / 2; 

//variaveis do oponente 
let xRaqueteOponente = 582;
let yRaqueteOponente = 150;

//velocidade da bolinha 
let velocidadeXbolinha = 6;
let velocidadeYbolinha= 6;

//variaveis da raquete 
let xRaquete = 5;
let yRaquete = 150; 
let raquetecomprimento = 10;
let raqueteAltura = 90;

//placar do jogo 
let meusPontos= 0;
let pontosDoOponente = 0;


//sons do jogo 
let raquetada;
let ponto;
let trilha;

let colidiu = false;

function setuo() {
createCanvas (600 , 400);
trilhas. loop ();}
{
  
  function draw () {
    background ( 0) ;
    mostraBolinha();
    movimentaBolinha();
    verificaColisaoBordada();
    mostraRaquete(xRaquete, yRaquete);
    movimentaMinhaRaquete();
    verificaColisaoRaquete(xRaquete, yRaquete);
    verificaColisaoRaquete(xRaqueteOponente, RaqueteOponente);
    mostraRaquete (xRaqueteOponente, yRaqueteOponente);
    movimentaRaqueteOponente ();
    incluiPlacar()
    marcaPonto();
  }
  function mostraBolinha (){
    circle (xBolinha, yBolinha, diametro);
  }
  
  function movimentaBolinha(){
xBolinha += velocidadeXBolinha;
yBolinha += velocidadeYBolinha;
  }
  
  function verificaColisaoBordada(){
    if (xBolinha + raio > width || xBolinha - raio < 0) {
      velocidadeXBolinha *= -1;
    }
    if (yBolinha + raio > height || yBolinha -raio < 0) {
      velocidadeYBolinha *= -1;
    }
  }

function mostraRaquete(x,y) {
  rect (x, y, raqueteComprimento,raqueteAltura);
}
  
function movimentaMinhaRaquete() {
  if(keyIsDown(UP_ARROW)){
    yRaquete -= 10;
  }
  if(keyIsDown(DOWN_ARROW)) {
    yRaquete +=10;
  }
}

  function verificaColisaoRaquete() {
  if (xbolinha - raio < xRaquete + raqueteComprimento && yBolinha - raio < yRaquete + RaqueteAltura && yBolinha + raio > yRaquete){
    velocidadeXBolinha *= -1;
    raquetada.play();
  }
  }

function verificaColisaoRaquete (x, y) {
  colidiu = collideRectCircle (x, y), raqueteComprimento,RaqueteAltura, xBolinha, yBolinha, raio) ;
  if (colidiu){
    velocidadeXBolinha 
  velocidadeXBolinha *= -1; 
    raquetada.play();
  }
}
  function movimentaRaqueteOponente(){
    if(keyIsDown(87)){
      yRaqueteOponente += 10;
    }
  if (keyIsDown(83)){
    yRaqueteOponente += 10;
  }
  }
  
  
  function incluiPlacar(){
    stroke(255)
    textAlign(CENTER);
    textSize(16);
    fill(color(255,140, 0));
    rect(150,10,40,20);
    fill(255);
    text(meusPontos,170,26);
    fill(color(255,140,0));
    rect(450,10,40,20);
    fill(255);
    text(pontosDoOponente, 470,26);
    
    
    
    
    
    
    function maraPonto(){
      if(xBoliha > 590) {
        meusPontos += 1;
        monto.play ();
      }
      if (xBolinha <10) {
      pontosDoOponnte += 1;
      pontos.play();
      }
    }
    
function preload(){
      trilha=loadSound("trilha.mp3");
      ponto = loadSound("ponto.mp3");
      raquetada= loadSound(raquetada.mp3");
}
    
