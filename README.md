# calculadora01
 ## projeto de uma calculadora que faz contas básicas

### Primeiramente, usei como base o seguinte esquema de calculadora:

![Imagem retirada do site FrreCodeCamp](./assets/0_7GfUdSILXBLyAbQy.png)

### Esta imagem é do site FreeCodeCamp que ensina como fazer uma calculadora com HTML, CSS e Javascript, mas assim como é sugerido no site, primeiramente estou tentando fazer sem olhar a resposta e seguindo a disposição de teclas como na imagem acima 

## Funcionamento da calculadora:

### basicamente, o programa da calculadora precisa "ouvir" as teclas com os números e as teclas que possuem os operadores aritméticos quando o usuário clica os botões, realizar o cálculo necessário e mostrar o resultado no display

há uma seção que é separada por uma tag div no htlm que engloba a calculadora no geral, uma div para cuidar do display, uma div para cuidar dos botôes e dentro dela mais uma **div class="calculadora_botoes"** que cuida diretamente dos botões da calculadora sendo então a classe calculadora_botoes onde está a tag pai dos botões.
Como está caixa (div) cuida diretamente dos botões da calculadora, então é nela em que será feita a configuração para que os botões fiquem posicionados no formato de grade. Isso é feito usando o **CSS Grid Layout** para criar um método bidimensional com linhas e colunas, fazemos isso dizendo que essa tag pai é um grid layout no nosso arquivo CSS:











