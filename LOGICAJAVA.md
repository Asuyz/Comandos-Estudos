• **Logica de programação em JAVA (lembretes, bons modos e explicação de funcionalidades de código).


° **Criação de classes
» Primeiro criamos os atributos (por exemplo: volume e estação):

**// Atributos**.

public (visibilidade) int (Ler números inteiros) volume;

public float (leitura de numero não inteiros) estacao;


**//Metodos**

public void (vazio) aumentarVolume() { 

|

|

}
public void diminuirVolume() {

|

|

}
publlic void trocarEstacao (float frequencia)  {

|

|

}

° **Testando a Classe**

» Para testar a classe precisamos primeiro criar um objeto.

**//método main para criar um botão para rodar o código**//Digite apenas "main e complete com o TAB"
public static void main(String[] args) { 

   Radio radio; //declaração do objeto radio
   
   radio = new Radio(); //instanciação do objeto
   
  radio.estacao = 89.1f (colocar o f para o java não confundir com um double)
  

  radio.volume = 5;
  
  radio.trocarEstacao (frequencia 92.5f);
  
  radio.aumentarVolume();
  
  radio.aumentarVolume();
  

System.out.println("Volume atual: " + radio.volume + "\nEstacao Atual: " + radio.estacao);

  //System out para mostrar o valor no console e /n para separar a linha.
  















°»