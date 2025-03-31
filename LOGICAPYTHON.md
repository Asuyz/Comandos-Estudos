° **Exemplo de utilização de if, elif e else:

```

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

