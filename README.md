# Linux_tutorial

## Se localizando no terminal utilizando <i>pwd<i>, <i>ls<i>, <i>mkdir<i>, <i>cd<i>, <i>man<i> e <i>help<i>.

A imagem abaixo representa uma janela do terminal.


![Screenshot from 2023-03-08 15-21-31](https://user-images.githubusercontent.com/46658489/223791482-39940e71-fa26-44e3-8705-205159d6fd11.png)


Repare a linha: (base) rafael@malaco:~$

Significado de cada item na linha acima:

(base): ignora isso agora. A gente vê isso depois.

rafael: usuário. O mesmo que você loga com sua senha.

malaco: nome do computador

~: caminho para o diretório atual. O diretório é a mesma coisa que a pasta no windows (err credo, pior sistema operacional). o charactere ~ indica o diretório de usuário.
Também conhecido como /home. Todos os seus arquivos e diretórios estão armazenados dentro deste diretório /home. A notação utilizada para descrever o diretório é a seguinte:

    /home/directory1/directory2/directory3

$: sei lá o que é isso

O coiso piscante: isso é o prompt. Quando ele está piscando, o terminal está disponível para receber comandos.

### Comando <i>pwd<i>

Para verificar o seu diretório atual, digite o comando <i>pwd<i>.

``` 
(base) rafael@malaco:~/Dropbox/working_folder_dropbox/Andrade_lab/Genomes$ pwd
/home/rafael/Dropbox/working_folder_dropbox/Andrade_lab/Genomes
```

### comando <i>ls<i>

Para listar os arquivos e diretórios presentes no diretório atual, utilize o comando <ls>.

```
(base) rafael@malaco:~/Dropbox/working_folder_dropbox/Andrade_lab/Genomes$ ls
AmpAmp  notebook_genomes.txt  PolPol  SacCar  SemBal
```

### opções de comandos

Normalmente, comandos podem aceitar ou exigir a utilização de opções. Apesar de cada comando ter formatos de opções diferentes, no geral, utiliza-se um dos seguintes formatos:
-opção1, --opção2, -o3.

Além das opções, algumas opções podem requerer valores. Estes valores podem ser um conjunto de characteres (ex. nome de um arquivo), ou um valor numérico (ex. uma fração).

Para verificar quais as opções disponíveis do comando <ls>, digite:

``` 
(base) rafael@malaco:~/Dropbox/working_folder_dropbox/Andrade_lab/Genomes$ ls --help
```
Na linha de comando acima, a opção --help é direcionada ao comando ls.

**Pergunta:** o que a linha de comanda acima retorna? Quais são as informações contidas no retorno da opção --help (preste atenção na linha que contem o 'usage'? 
Como esta opção é útil no cotidiano do bioinformata?

Digite no prompt o seguinte comando:

``` 
(base) rafael@malaco:~/Dropbox/working_folder_dropbox/Andrade_lab/Genomes$ ls -l -h -a
total 36K
drwxrwxr-x  6 rafael rafael 4,0K fev 14 14:37 .
drwxr-xr-x 10 rafael rafael 4,0K fev 14 12:49 ..
drwxrwxr-x  2 rafael rafael 4,0K fev 13 12:03 AmpAmp
-rw-rw-r--  1 rafael rafael 8,5K mar  7 17:30 notebook_genomes.txt
drwxrwxr-x  2 rafael rafael 4,0K fev 13 14:06 PolPol
drwxrwxr-x  2 rafael rafael 4,0K mar  8 13:58 SacCar
drwxrwxr-x  3 rafael rafael 4,0K fev 14 14:41 SemBal
```

**Pergunta:** utilizando os retorno da opção '--help', quais são as funções das opcoes -l, -h e -a?
Obs: arquivos ocultos começam com o character '.'.

Digite o seguinte comando:
```
(base) rafael@malaco:~/Dropbox/working_folder_dropbox/Andrade_lab/Genomes$ ls -lha
```
**Pergunta:** qual a diferença entre este comando e o comando anterior?

Cada coluna do retorno desta linha de comando é um detalhe do arquivo. Veja a figura abaixo:

![Screenshot from 2023-03-08 17-01-02](https://user-images.githubusercontent.com/46658489/223824854-240ba39c-94e4-488a-ac3c-5b050ccd1383.png)

**Permissões:** as permissões são descrições de quais ações o presente usuário pode efetuar com o arquivo. Exemplos de permissões são: escrever (alterar) e executar o arquivo.

**Tamanho:** o tamanho do arquivo, quando a opção -h é dada, é medida em B, kB, GB, TB.

**Data de criação:** Dá a data e a hora de criação do arquivo. Um detalhe importante é que a hora de criação é a hora em que o arquivo foi alterado pela última vez.


## Utilizando o Google: sim, eu tô ensinando isso!

Em programação a ferramenta mais efetiva é o Google. É muito comum que o programador não saiba como realizar uma determinada tarefa, o significado do retorno de um comando ou como utilizar um comando específico.
Para isso temos o Google!

Mas não é tão fácil assim. Pesquisar conteúdos de programação no Google requer um pouco de prática e paciência para achar os termos certos.

**Atividade:** procure no google o que as outras colunas retornadas da linha de comando acima significam.

## Criando e navegando por diretórios. mkdir, cd.

Para trabalhar com as linhas de comando, umas das principais atividades é navegar pelos diretórios. Navegar pelos diretórios significa mudar o diretório atual, aquele que você está. Para navegar pelos seus diretórios, nós vamos criar um novo diretório, chamado 'new_directory'. Após o novo diretório ser criado nós vamos mudar de diretório para criar novos arquivos neste 'new_directory'.


Para checar qual é diretório atual, use o comando pwd apresentado anteriormente.

```
(base) Rafaels-MacBook-Pro:~ rafael$ pwd
```

**Pergunta:** qual é o seu diretório atual?

Para criar um novo diretório, utilize o comando mkdir

```
(base) Rafaels-MacBook-Pro:~ rafael$ mkdir new_directory

```

**Pergunta:** como você pode checar se o novo diretório foi criado?

Para mudar o seu diretório atual para o novo diretório, utilize o comando cd.

```
(base) Rafaels-MacBook-Pro:tutorial1_linux rafael$ cd new_diretory
```
**Pergunta:** como você pode checar se está no diretório desejado?


É importante notar, o comando cd obedece a seguinte estrutra: cd [directory_path]

O path the de um arquivo ou diretório é todo o caminho utilizado para chegar até um determinado arquivo ou diretório. 

Por exemplo: 

/home/rafael/Dropbox/working_folder_dropbox/Andrade_lab/Genomes

Esta linha indica que o diretório 'Genomes' está dentro do diretório 'Andrade_lab' e assim por diante.

Contudo, o prompt assume o path do seu diretório atual, e por isso você não precisa digitar o caminho inteiro de arquivos e diretórios que estão dentro do seu diretório atual. Esta regra serve tanto para o comando cd, como para outros comandos.

Por exemplo:

```
(base) Rafaels-MacBook-Pro:new_diretory rafael$ cd ~/Users/rafael/Dropbox/working_folder_dropbox/Andrade_lab/IC/tutorial1_linux/new_diretory

(base) Rafaels-MacBook-Pro:new_diretory rafael$ cd new_diretory
```

Ambos os comandos acima, são equivalentes caso você esteja no diretório 'Tutorial1_linux', mas são diferentes se você estiver em outro diretório.



