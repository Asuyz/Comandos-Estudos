° **Utilização de if, elif e else**:

» **If, elif e else** são estruturas condicionais. Estruturas condicionais são seções onde definem condições para a execução de determinados blocos de comandos (ao invés de executa-los todos de uma o programa para e decide qual caminho seguir baseada na condição do momento).

» Basicamente se **X** condição for satisfeita, execute **esse** bloco de comandos, **senão** execute outro bloco de comandos.

» O **elif** é uma estrutura intermediária dentro da seção if-else no python e deve vir como um complemento a ambos. Quando você já tem um IF e um ELSE, mas precisa de uma condição para especificar outra regra, pode usar o elif.

° **Exemplos**:

```
"""
Com base na idade permitir ou não a coleta de sangue. (o código pode se tornar mais complexo pois existe a exceção de pessoas cadastradas antes dos 60 anos poderem doar sangue mesmo não cumprindo a idade maxima dos mesmos 60 anos).

"""

print ("Olá muito obrigado por escolher doar sangue. Digite a sua idade:")

idade = int(input())

  

if 18 <= idade <=60:

    print ("Você é valido para a doação de sangue, se desloque para a unidade mais proxima!")

  

elif 16<= idade <= 17:

    #Criação de um bloco if e else dentro de um elif (Com a identação utilizada de forma correta, onde o if e else pertence ao elif)

    print ("Você tem autorização dos seus responsaveis para doar? Digite S ou N.")

    autorização = input()

  

    if autorização == "S":

        print ("Se encaminhe para a unidade mais proxima. Agradecemos o gesto.")

  

    else:

        autorização == "N"

        print ("Agradecemos o gesto, porém você ainda não pode doar.")

#Aqui voltamos ao primero bloco (if, elif e o else:) para a finalização do código

else:

    print ("Você não pode doar.")
   
```

```
#calculadora que seleciona os operadores (Apenas no terminal).

  
print ("Selecione o seu operador: +,-,/,*")

operador =input()

  

print ("Digite um número a sua escolha:")

num1 = float(input())

print ("Digite outro número:")

num2 = float(input())

  
  

if operador == "+":     #if, elif e else sempre estão são atreladas em condições

    num1 + num2

    print (num1 + num2)

elif operador == "-":

    num1 - num2

    print (num1 - num2)

  

elif operador == "/":

    num1 / num2

    print (num1 / num2)

  

elif operador == "*":

    num1 * num2

    print (num1 * num2)

else:

    print ("Operador Inválido (Selecione entre: +, -, * ou ;).")

```

° **Base de um programa com JANELA**:

```
#criacao de uma interface (sem programa, apenas a janela).

import requests #Import de biblioteca no https://pypi.org

from tkinter import *

  

janela_1 =Tk()

  

janela_1.title("janela")

  

janela_1.mainloop()
```