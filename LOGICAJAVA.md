• **Logica de programação em JAVA (lembretes, bons modos e explicação de funcionalidades de código).


° **Criação de classes

» **Primeiro criamos os atributos (por exemplo: volume e estação):**


```
package br.com.fiap;  
  
public class Radio {  
      //atributos  
    public int volume;  
    public float estacao;  
    //metodos  
    public void aumentarVolume() {  
        volume++;  
    }  
    public void diminuirVolume() {  
        volume--;  
    }  
    public void trocarEstacao (float frequencia) {  
        estacao = frequencia;  
    }  
  
}

```

» **Criação do objeto para testes (No caso objeto RADIO)**:

```
package br.com.fiap;  
  
public class TesteRadio {  
  
    public static void main(String[] args) {  
        //para testar a classe precisamos criar um objeto  
        Radio radio; //declaracao do objeto radio  
        radio = new Radio(); //instanciacao do objeto (usamos new)  
        radio.estacao = 89.1f;  
  
        radio.volume = 5;  
        radio.trocarEstacao(192.5f);  
        radio.aumentarVolume();  
        radio.aumentarVolume();  
  
        System.out.println("Volume atual: " + radio.volume + "\nEstacao Atual: " + radio.estacao);  
    }  
  
}
```








°»