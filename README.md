# calculadora01
 ## projeto de uma calculadora que faz contas básicas

### Primeiramente, usei como base o seguinte esquema de calculadora:

![Imagem retirada do site FrreCodeCamp](./assets/0_7GfUdSILXBLyAbQy.png)

### Esta imagem é do site FreeCodeCamp que ensina como fazer uma calculadora com HTML, CSS e Javascript, mas assim como é sugerido no site, primeiramente estou tentando fazer sem olhar a resposta e seguindo a disposição de teclas como na imagem acima 

## Funcionamento da calculadora:

### basicamente, o programa da calculadora precisa "ouvir" as teclas com os números e as teclas que possuem os operadores aritméticos quando o usuário clica os botões, realizar o cálculo necessário e mostrar o resultado no display

há uma seção que é separada por uma tag div no htlm que engloba a calculadora no geral, uma div para cuidar do display, uma div para cuidar dos botôes e dentro dela mais uma **div class="calculadora_botoes"** que cuida diretamente dos botões da calculadora sendo então a classe calculadora_botoes onde está a tag pai dos botões.
Como está caixa (div) cuida diretamente dos botões da calculadora, então é nela em que será feita a configuração para que os botões fiquem posicionados no formato de grade. Isso é feito usando o **CSS Grid Layout** para criar um método bidimensional com linhas e colunas, fazemos isso dizendo que essa tag pai é um grid layout no nosso arquivo CSS:

![Imagem de formando o cssgridlayout](./assets/gridlayout1.png)


agora que a div referente a esta classe **class="calculadora_botoes** se tornou um display grid, todos os seus filhos, nocaso as tags button referente aos botões da calculadora se tornam **grid items**

Neste momento, a aparência está desta forma:

![Imagem de formando o cssgridlayout](./assets/depoisdegridlista.png)

Como podemos observar pela imagem, mesmo dizendo que se trata de um grid, está se comportando ainda como uma lista com item abaixo de item, no caso botão abaixo de botão. Para deixarmos como com linhas e colunas, vamos definir as **trilhas de colunas** usando a propriedade **grid-template-columns**


![Imagem da formação de colunas](./assets/trilhacoluna.png)


Aqui está sendo dito a partir desta propriedade grid-template-columns que é necessário formar 4 colunas de 1fr cada uma, por isso foi repetido o valor quatro vezes. A unidade de medida fr seria uma fração do espaço disponível no grid.
Depois disso, o resultado fica desta forma:

![Imagem da formação de colunas](./assets/colunacomfr.png)

Como as linhas estão um tanto quanto pequenas, vamos mudar seu tamanho a partir da propriedade **grid-auto-rows** que define o tamanho padrão para as linhas criadas no grid e aqui será colocoado o valor de 50px:

![Imagem da formação de colunas com tamanho maior](./assets/autorows.png)

E as linhas dos grid items ou botões da calculadora ficam maiores:

![Imagem da formação de colunas com tamanho maior](./assets/botaomaior.png)


Como podemos ver na imagem inicial que está sendo usada como base, a disposição dos botões no grid ainda não está igual. O botão que representa o sinal de = tem um tamanho e disposição diferente dos demais. Então para tratar isso, fiz uma classe específica para ele no html para que este botão possa ter sua própria estilização, ele receberá uma classe própria que é **class="box1"**:

![Imagem da formação do botão =](./assets/botao=class.png)


No arquivo CSS, será feito sua estilização dizendo através da propriedade **grid-column-start:** que este botão começará na coluna 4 e através da propriedade **grid-row-start:** que começará na linha 2 e pela **grid-row-end:** que terminará na linha 6, no caso na fração de espaço disponível no grid.

![Imagem da formação do botão =](./assets/box1coluna.png)

O resultado ficará com esta aparência:

![Imagem da formação da calculadora](./assets/calculadoraresult.png)

## Estilização do display 

### Por enquanto, o display aparece com o número 0, mas normalmente ão é dessa forma que fica o display de uma calculadora antes de aparecer o resultado do cálculo realizado, então vamos mudar esta estilização 

Vamos modificar no arquivo html onde estava este 0, no caso dentro da tag h1, vamos colocar **class="display_piscar"** e no lugar do número 0 vamos colocar o pipe |
No arquivo CSS, será colocado a estilização para fazer o pipe piscar:

![Imagem da formação do display](./assets/pipesimbolo.png)

A aparência final da calculadora já está pronta, mas ela ainda não funciona. Para isso, vamos criar suas funcionalidades com JavaScript.


## Funcionalidade da calculadora

Para serem feitas as interações, primeiramente será criado o arquivo JavaScript app.js e linkado no html através da tah script

![Imagem de linkando o arquivo javascript](./assets/linkandojs.png)


Agora para fazer a calculadora funcionar e interagir com os comandos do usuário, vamos colocar os códigos dentro deste arquivo app.js





































