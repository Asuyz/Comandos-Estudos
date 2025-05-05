## • **Logica de programação em JAVA (lembretes, bons modos e explicação de funcionalidades de código).

## ° **Criação de classes

» **Primeiro criamos os atributos (por exemplo: volume e estação):**

```js
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

```js
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

## ° **Scanner**

» A classe `Scanner` permite capturar entradas de texto, números inteiros, números de ponto flutuante, entre outros. Segue exemplos:

» Primeiro criamos a classe com os atributos e métodos:

```js
package br.com.fiap.bean;  //Separamos os pacotes das classes entre bean e main
  
public class FolhaDePagamento {  
    public double salarioBruto;  
    public int numeroDeDependentes;  
    public double descontoINSS;  
    public double valorPlanoDeSaude;  
    
    // Atributos - A variavel sempre será descrita no diagrama (Double, Int, Float etc)
  
    // Metodos - Procure dividir o problema para uma maior facilidade de racicinio (desconto1 e desconto2)
    
    public double calcularSalarioliquid(){  
        double desconto1, desconto2, salarioLiquido; //Dividindo o problema (calcular salario liquido) em pequenas solucoes  
  
        desconto1 = salarioBruto * (descontoINSS / 100 );  
        desconto2 = valorPlanoDeSaude * (numeroDeDependentes + 1 );  
        salarioLiquido = salarioBruto - (desconto1 + desconto2);  
  
  
        return salarioLiquido;  
    }  
  
}

```

» Depois criamos o método main para testar (rodar) a classe criada:

```js
package br.com.fiap.main;  
  
import br.com.fiap.bean.FolhaDePagamento; // O import acontece quando declaramos o objeto 
  
public class FolhaDePagamentoMain {  
  
        public static void main(String[] args) {  
            FolhaDePagamento folha = new FolhaDePagamento();  
            // Declaração do objeto // Instanciação do objeto  
            folha.salarioBruto = 10000;  
            folha.descontoINSS = 15;  
            folha.numeroDeDependentes = 3;  
            folha.valorPlanoDeSaude = 500.0;  
  
            System.out.printf(  
                    "Salario bruto: R$ %.2f\n" +  
                            "Dependentes: %d\n" +  
                            "INSS: %.1f%%\n" + // O "%%" é para exibir o símbolo de porcentagem  
                            "Valor Plano de Saúde: R$ %.2f\n" +  
                            "Salário líquido: R$ %.2f\n", // Formatação para o salário líquido  
                    folha.salarioBruto, folha.numeroDeDependentes, folha.descontoINSS,  
                    folha.valorPlanoDeSaude, folha.calcularSalarioliquid());  
        }  
    }

```

» Agora para a classe scanner:

```js
package br.com.fiap.main;  
  
import br.com.fiap.bean.FolhaDePagamento; 
  
import java.util.Scanner; // Import do scanner 
  
public class MainScanner {  
    public static void main(String[] args) {  
        FolhaDePagamento folha = new FolhaDePagamento();  
        Scanner scanner = new Scanner(System.in); //Declaração e instanciação dos dois imports
         try {  
  
  
             System.out.println("Digite o salario bruto:");  
             folha.salarioBruto = scanner.nextDouble(); // scanner e a variavel para armazernar a opção digitada (console)
  
             System.out.println("Digite o valor do plano de saude:");  
             folha.valorPlanoDeSaude = scanner.nextDouble();  
  
             System.out.println("Digite o N de Dependentes:");  
             folha.numeroDeDependentes = scanner.nextInt();  
  
             System.out.println("Digite o Desconto INSS:");  
             folha.descontoINSS = scanner.nextDouble();  
  
             System.out.println("Salario Liquido: %2.f" + folha.calcularSalarioliquid());  
  
  
         } catch (Exception e) { //Try e catch para analizar os erros (exceções dos atributos) 
             System.out.println("Formato de Numero Incorreto");  
         }  
        finally { //finally para rodar o scanner.close independente de erros
             scanner.close(); // Boa pratica sempre realizar o fechamento do scanner para evitar vazamentos de mémoria 
         }  
    }  
}
```

° Embora seja possível colocar os atributos diretamente no código `main`, a abordagem correta seria tratá-los através de métodos `setter` e `getter` (Aprendizagem futura), seguindo os princípios de **encapsulamento** da programação orientada a objetos. Isso torna o código mais modular, reutilizável e fácil de manter.

```js
package br.com.fiap.main;  
  
import br.com.fiap.bean.FolhaDePagamento;  
  
import java.util.Scanner;  
  
public class MainScanner {  
    public static void main(String[] args) {  
        FolhaDePagamento folha = new FolhaDePagamento();  
        Scanner scanner = new Scanner(System.in);  
        double salarioBruto;  
        int numeroDeDependentes;  
        double descontoINSS;  
        double valorPlanoDeSaude;
```

## **° JOptionPane:**

» A função **`JOptionPane.showInputDialog`** é usada para capturar as entradas do usuário. Cada vez que o programa pede um valor, ele exibe uma caixa de diálogo onde o usuário pode digitar o valor.

» Como o valor recebido do `JOptionPane` é sempre uma string, usamos **`Double.parseDouble`** para converter as entradas de texto em valores numéricos (`double` ou `int` conforme o tipo necessário).

° Como irá funcionar:

» Ao executar o programa, ele vai pedindo os valores ao usuário por meio de caixas de entrada (caixas de diálogo) do **`JOptionPane`**.

» Após o preenchimento dos campos, o cálculo do salário líquido é realizado e o resultado é mostrado em uma nova caixa de mensagem.

» Se o usuário inserir dados inválidos (como texto quando é esperado um número), o programa mostra uma mensagem de erro.

```js
import br.com.fiap.bean.FolhaDePagamento;
import javax.swing.*;

public class MainJOptionPane {
    public static void main(String[] args) {
        try {
            // Solicitar o salário bruto
            String salarioBrutoStr = JOptionPane.showInputDialog(null, "Digite o Salário Bruto:");
            double salarioBruto = Double.parseDouble(salarioBrutoStr);  // Converte a entrada para double

            // Solicitar o valor do plano de saúde
            String valorPlanoSaudeStr = JOptionPane.showInputDialog(null, "Digite o valor do plano de saúde:");
            double valorPlanoSaude = Double.parseDouble(valorPlanoSaudeStr);

            // Solicitar o número de dependentes
            String numeroDependentesStr = JOptionPane.showInputDialog(null, "Digite o número de dependentes:");
            int numeroDeDependentes = Integer.parseInt(numeroDependentesStr);

            // Solicitar o desconto INSS
            String descontoINSSStr = JOptionPane.showInputDialog(null, "Digite o desconto INSS (em %):");
            double descontoINSS = Double.parseDouble(descontoINSSStr);

            // Criar a instância da classe FolhaDePagamento e calcular o salário líquido
            FolhaDePagamento folha = new FolhaDePagamento();
            folha.salarioBruto = salarioBruto;
            folha.valorPlanoDeSaude = valorPlanoSaude;
            folha.numeroDeDependentes = numeroDeDependentes;
            folha.descontoINSS = descontoINSS;

            // Calcular o salário líquido
            double salarioLiquido = folha.calcularSalarioliquid();

            // Exibir o resultado em um JOptionPane
            JOptionPane.showMessageDialog(null, String.format("Salário Líquido: R$ %.2f", salarioLiquido));

        } catch (NumberFormatException ex) {
            // Caso ocorra um erro de formatação (entrada inválida), mostrar uma mensagem de erro
            JOptionPane.showMessageDialog(null, "Erro: Por favor, insira valores numéricos válidos.", "Erro", JOptionPane.ERROR_MESSAGE);
        }
    }
}
```

## ° **Javax.swing:**

» **`import javax.swing.*;`** importa **todas** as classes e interfaces do pacote **`javax.swing`**, permitindo que você use os componentes gráficos que essa biblioteca oferece, sem precisar importar cada classe individualmente.

» O asterisco (`*`) é um **curinga** que significa "todos os componentes" dentro do pacote.

Exemplos de componentes Swing mais usados:

» **`JFrame`:** A janela principal da aplicação gráfica.

» **`JButton`:** Um botão clicável.

» **`JLabel`:** Um rótulo de texto.

»  **`JTextField`:** Um campo de entrada de texto.
 
» **`JOptionPane`:** Uma caixa de diálogo simples (muito útil para mostrar mensagens ou capturar 
 entradas do usuário).
 
» **`JCheckBox`:** Uma caixa de seleção.
 
 » **`JRadioButton`:** Botões de opção (radio buttons).

» **`JPanel`:** Um painel para organizar outros componentes na tela.

» **`import javax.swing.*;`** importa todas as classes da biblioteca Swing.

» Com isso, você pode criar interfaces gráficas ricas e interativas em Java, como janelas, botões, caixas de texto, menus, etc.

» **Swing** é amplamente utilizado em Java para criar aplicações desktop com interfaces gráficas.

° **PrintF e PrintLn
 
» **PrintF** é necessário passar dois paramentos nesse print.

» **PrintLn** é necessário apenas um parametro (vai printar uma nova linha de texto no console).

----------------------------------------------------------------

## ° **Encadeamento de Métodos: Uso de um Método Dentro de Outro**

° **Exemplo de Utilização de um Método dentro de outro Método**:

```js
package br.com.fiap.bean;  
  
public class DespesaFamiliar {  
    //Atributos  
    public double rendaFamiliar; // Total que a familia recebe  
    public int numeroDeMoradores; // Total de moradores  
    public double gastoComLuz; // Gasto Mensal com Luz  
    public double gastoComAgua; // Gasto Mensal com Agua  
    public double gastoComInternet; // Gasto Mensal com Internet  
    public double valorMensalidadeDaAcademia; // Valor da mensalidade da academia (multiplicar pelo numero de membros)  
  
  
    //Metodos: calcularTotalDeDespesas e calcularRendaFamiliarLiquida  
    public double calcularTotalDeDespesas(){  
        double resultado1, resultado2;  
  
        resultado1 = gastoComAgua + gastoComInternet + gastoComLuz;  
        resultado2 = numeroDeMoradores * valorMensalidadeDaAcademia;  
  
        return resultado1 + resultado2;  
  
    }  
    public double calcularRendaFamiliarLiquida(){  
        double despesasTotais = calcularTotalDeDespesas(); //Trouxe o metodo calcularTotalDespesas dentro desse metodo  
  
        return rendaFamiliar - despesasTotais;  
  
  
    }  
  
}
```

» **Execução do Objeto**:

```js
package br.com.fiap.main;  
  
import br.com.fiap.bean.DespesaFamiliar;  
  
import java.util.Scanner;  
  
public class DespesaFamiliarMain {  
    public static void main(String[] args) {  
        Scanner scanner = new Scanner(System.in); //System In = System Input (Para gravar os dados digitados)  
        DespesaFamiliar despesa = new DespesaFamiliar();  
  
  
        try {  
  
            System.out.println("Digite a sua renda familiar Total: ");  
            despesa.rendaFamiliar = scanner.nextDouble();  
  
            System.out.println("Digite o numero de membros da familia: ");  
            despesa.numeroDeMoradores = scanner.nextInt();  
  
            System.out.println("Digite o valor da academia: ");  
            despesa.valorMensalidadeDaAcademia = scanner.nextDouble();  
  
            System.out.println("Digite o valor do gasto de agua: ");  
            despesa.gastoComAgua = scanner.nextDouble();  
  
            System.out.println("Digite o valor do gasto de Luz: ");  
            despesa.gastoComLuz = scanner.nextDouble();  
  
            System.out.println("Digite o valor do gasto de internet: ");  
            despesa.gastoComInternet = scanner.nextDouble();  
  
            double rendaFamiliar = despesa.rendaFamiliar;  
            System.out.printf("Renda da familia: R$ %.3f%n" , rendaFamiliar);  
  
            double rendaLiquida = despesa.calcularRendaFamiliarLiquida();  
            System.out.printf("Renda familiar líquida: R$ %.3f%n", rendaLiquida);  
  
            double totalDespesas = despesa.calcularTotalDeDespesas();  
            System.out.printf("Despesas totais: R$ %.3f%n", totalDespesas);  
  
  
        } catch (Exception e) {  
            System.out.println("ERRO AO CALCULAR");  
        }        finally {  
            scanner.close();  
    }   } }

```

° **Exemplo do mesmo código criando variáveis e passar o valor da variável ao objeto: **

```js
package br.com.fiap.main;  
  
import br.com.fiap.bean.DespesaFamiliar;  
  
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        DespesaFamiliar despesaFamiliar = new DespesaFamiliar();  
        double rendaFamiliar, gastoComLuz, gastoComAgua, gastoComInternet, valorMensalidadeDaAcademia;  
        int numeroDeMoradores;  
        Scanner scanner = new Scanner(System.in);  
  
        try {  
            System.out.print("Digite o valor da renda familiar: ");  
            rendaFamiliar = scanner.nextDouble();  
  
            System.out.print("Digite o número de moradores: ");  
            numeroDeMoradores = scanner.nextInt();  
  
            System.out.print("Digite o valor do gasto com luz: ");  
            gastoComLuz = scanner.nextDouble();  
  
            System.out.print("Digite o valor do gasto com água: ");  
            gastoComAgua = scanner.nextDouble();  
  
            System.out.print("Digite o valor do gasto com internet: ");  
            gastoComInternet = scanner.nextDouble();  
  
            System.out.print("Digite o valor da mensalidade da academia: ");  
            valorMensalidadeDaAcademia = scanner.nextDouble();  
  
            despesaFamiliar.rendaFamiliar = rendaFamiliar;  
            despesaFamiliar.numeroDeMoradores = numeroDeMoradores;  
            despesaFamiliar.gastoComLuz = gastoComLuz;  
            despesaFamiliar.gastoComAgua = gastoComAgua;  
            despesaFamiliar.gastoComInternet = gastoComInternet;  
            despesaFamiliar.valorMensalidadeDaAcademia = valorMensalidadeDaAcademia;  
  
            System.out.printf("Registros:\nRenda familiar: R$ %.3f\nTotal de gastos com despesas: R$ %.3f\nRenda familiar líquida: R$ %.3f", despesaFamiliar.rendaFamiliar, despesaFamiliar.calcularTotalDeDespesas(), despesaFamiliar.calcularRendaFamiliarLiquida());  
        } catch (Exception e) {  
            System.out.println("Informe as credencias corretas!");  
        }  
    }  
}
```








°»
