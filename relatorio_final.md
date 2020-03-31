# Relatório Final - Horse Colic Data Set
> Disciplina: **Data Mining**
> Aluno: **Antonioni Barros Campos**
> Contato: **(81) 99104-7437**
> Email: antonioni.campos@gmail.com
> Professora: **Manoela Kohler**

## Introdução

O projeto sugerido foi o de classificação da chance de sobrevivência de cavalos baseados em suas condições médicas. Originalmente, os dados são representados por 27 atributos que são explicados no arquivo `datadict.pdf` e possuem 368 instâncias no total.  

Para o projeto, foram fornecidos dois grupos de dados: 1 data set de treinamento com 299 instâncias (representado em `horse.csv`) e 1 data set de teste com 89 instâncias (representado em `horseTest.csv`).  

O estudo do data set foi feito em Python e o código está no arquivo `analise.ipynb`.

## Análise dos dados

Inicialmente, foram carregados os arquivos .csv (todas as análises dos dados nos arquivos foram feitas utilizando a biblioteca pandas).   

Em seguida, foi feita uma exploração dos dados. Dos 27 atributos, foi constatado que 7 atributos eram valores numéricos enquanto o restante eram dados categóricos.  

A primeira operação feita no data set foi de retirada do atributo `cp_data` devido ao fato de que essa variável não tem significância devido aos dados de patologia não são incluídas e coletadas nesses casos.  

Depois, foi feito um filtro de valores faltantes (NA) e constatou-se que existiam muitos atributos com valores em falta. O atributo com mais alto número de NA foi o atributo `nasogastric_reflux_ph` com 246 de 299 valores faltantes. Nesse caso, foi decidido retirar esse atributo do data set por não ter condições de representar sua contribuição na modelagem. 

Após,  foi decidido retirar também o atributo `hospital_number` devido a sua alta cardinalidade e não trazer nenhuma contribuição nos seus dados.

Finalmente, foram retirados os atributos `lesion_2` e `lesion_3` por terem variabilidade quase inexistente (enquanto `lesion_2` possuía apenas 7 eventos diferentes de zero, `lesion_3` possuía apenas 1)
