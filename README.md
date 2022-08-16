# Cereal80
A ideia desse projeto foi botar em prática meu aprendizado em ciência de dados, utilizando Python no Google Colab.

O Dataset escolhido foi sobre cereais consumidos nos Estados Unidos.
 Selecionei ele em um guia com os Datasets mais interessantes para iniciantes, vou deixar aqui o link: https://www.kaggle.com/code/rtatman/fun-beginner-friendly-datasets/notebook

E aqui um link direto para o Dataset: https://www.kaggle.com/datasets/crawford/80-cereals

Deixarei um link aqui com os insights que consegui desses dados: https://medium.com/@VitorMello./uma-an%C3%A1lise-sobre-o-mercado-atual-de-cerais-4cf36d5ec6c7

## Algumas observações a fazer:

+ Foquei nas fabricantes para fazer uma análise exploratória, utilizando os teores calóricos de seus cereais e suas respectivas notas de consumidores.

+ Aqui está a qual fabricantes as letras pertencem: 

A = American Home Food Products

G = General Mills

K = Kelloggs

N = Nabisco

P = Post

Q = Quaker Oats

R = Ralston Purina

+ Na coluna "type" há somente dois valores possíveis, que remetem para o modo de consumo de cada cereal: "H" para quente; "C" para frio. 

### Sobre as etapas de desenvolvimento:

+ Primeira etapa: importei as bibliotecas e os dados. Para os dados escolhi uma abordagem oferecida pelo Colab, que auxilia no upload do Dataset diretamente de sua máquina, inclusive por este motivo importei a biblioteca "IO", para a leitura desses dados.

+ Segunda etapa: onde fiz a limpeza dos dados minha maior preocupação era com a última coluna, a de "ratings" (notas), ela era toda seguida por ponto e vírgula, isso causava dois problemas: além da estranha visualização de números seguidos por ponto e vírgula (Exemplo: 12.345;;); também ocasionava na leitura do programa, que entendia ele como uma string e não como float.

+ Terceira etapa: minha ideia foi comparar o número de cereais por fábrica, utlizando a função value_counts() e plotando um gráfico.

+ Quarta etapa: decidi abordar um pouco sobre a coluna "type", porém, apenas três cereais de toda a tabela eram consumidos quente e não haviam correlações entre eles.

+ Quinta etapa: analisando as calorias, utilizei funções como describe(), para descobrir a média, a mediana, o minímo e máximo. Também utilizei as funções nlargest() e nsmallest() para encontrar as 5 melhores e piores notas. Por último verifiquei a média calórica por fábrica com a função groupby() e plotando um gráfico.

+ Sexta etapa: analisei as notas com uma abordagem parecida com as calorias, decidi diminuir a o número de casas decimais para uma melhor visualização com a função round().

+ Sétima etapa: na última etapa queria também calcular a média de nota por fábrica, porém dessa vez foi necessário criar um novo DataFrame, com a função to_frame(), e por último plotar um gráfico utilizando a biblioteca seaborn.
