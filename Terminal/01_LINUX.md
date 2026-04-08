
» Diretórios essenciais

| ***Diretório*** | ***Função***                                               | ***Exemplo***        |
| --------------- | ---------------------------------------------------------- | -------------------- |
| **/bin**        | Executáveis essenciais disponíveis a todos os usuários     | ls, cp               |
| **/sbin**       | Executáveis de administração de sistema(root)              | ifconfig , iptables  |
| **/etc**        | Arquivos de configuração global                            | /etc/ssh/sshd_config |
| **/home**       | Diretórios pessoais dos usuários                           | /home/user           |
| **/var**        | Dados váriaveis(logs,spool)                                | /var/log/syslog      |
| **/usr**        | Programas de usuário, manuais e bibliotecas compartilhadas | /usr/bin/grep        |
| **/tmp**        | Arquivos temporários limpos em reinicialização             | /tmp/socket          |

» Deslocamento pelo Sistema

| ***Comando***     | ***Desc***                                        | ***Exemplo*** |
| ----------------- | ------------------------------------------------- | ------------- |
| **pwd**           | Mostra o diretório atual                          | pwd           |
| **cd**            | Troca de diretório                                | cd, cd..      |
| **ls (-l -a -h)** | Lista o conteúdo(longa,ocultos,tamanhos legíveis) | ls -lah       |
| **exit**          | Fecha o terminal                                  | --            |
| **clear**         | Limpa o terminal                                  | --            |

» Criação, Cópia e Remoção  

| ***Comando***  | ***Ação***                                                 | ***Exemplo***                 |
| -------------- | ---------------------------------------------------------- | ----------------------------- |
| **mkdir**      | Cria novo diretório                                        | mkdir projetos                |
| **touch**      | Cria um arquivo vazio (escolha o tipo com o .tipo_arquivo) | touch calc.py                 |
| **echo**       | Exibe um teste no terminal                                 | echo "123teste" > arquivo.txt |
| **cp (-r)**    | Copia arquivos ou pastas                                   | cp foto.jpg ~/backup/         |
| **mv**         | Move ou renomeia                                           | mv notas.txt notas_old.txt    |
| **rm (-r -f)** | Remove(recursivo,forçado)                                  | rm -rf tmp/                   |

↪ No uso de **echo**: ***>*** (Cria um novo arquivo - sobreposição) e ***>>*** (Adiciona o conteúdo ao arquivo).


» Visualização de Conteúdo

| ***Comando***    | ***Desc***                                  | ***Exemplo***        |
| ---------------- | ------------------------------------------- | -------------------- |
| **cat**          | Exibe arquivo inteiro                       | cat read.me          |
| **less**         | Rolagem interativa, ideal para logs grandes | less install.log     |
| **head/tail -n** | Primeiras ou últimas linhas                 | tail -10 install.log |

» Administração do Sistema

| ***Comando*** | ***Desc***                               | ***Exemplo***                             |
| ------------- | ---------------------------------------- | ----------------------------------------- |
| **find**      | Localizar arquivos específicos no SO     | find .-name "*.txt"                       |
| **grep**      | Buscar textos dentro dos arquivos        | grep "ERROR" logs/*.log                   |
| **df**        | Monitorar o espaço disponível no sistema | df -Th                                    |
| **ps**        | Lista processos no sistema               | ps -aux \| grep (< processo a procurar >) |
| **top**       | Monitora o Sistema em Tempo Real         | top -u admlnx                             |

↪ em **find** o ponto significa o diretório corrente no Linux.

