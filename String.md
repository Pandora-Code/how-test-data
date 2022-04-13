
<p align="center">
 <img width="200px" src="https://avatars.githubusercontent.com/u/87428056?s=200&v=4" align="center" alt="pandora-code" />
 <h2 align="center">Campo de Texto</h2>
</p>

Esse é um tipo básico, porém dependendo dos requisitos do seu cliente ele pode ter regras a mais que vão gerar mais verificações. Vamos analisar algumas perguntas a respeito desse tipo de dado

1. O texto tem limite de tamanho mínimo ou máximo?
2. Aceita valores númericos?
3. Aceita caracteres especiais?
4. Aceita valores só em caixa alta ou caixa baixa?
5. Deve ser preenchido em um formato específico para aceitar o dado ou já é atribuida uma formatação ao inserir o dado?

> Vale ressaltar que cada um dessas questões vão levar a um ou mais testes a serem realizados, alguns deles podem ser realizados em conjunto, dependendo do critério de aceite do dado.

#### 1. O texto tem limite de tamanho mínimo ou máximo?

Caso o texto possua valor mínimo ou/e máximo, para cada um você irá realizar um teste para os valores limite.

Caso possua o valor possua apenas um tamanho mínimo, seus valores serão: Dado que Min é o limite mínimo, então Min-1 e Min
Caso possua o valor possua apenas um tamanho máximo, seus valores serão: Dado que Max é o limite máximo, então Max e Max+1
Caso ele possua um possua um tamanho mínimo e máximo, seus valores serão: Dado que Min é o limite mínimo e Max é o limite máximo, então Min-1, Min, Max e Max+1.

#### 2. Aceita valores númericos?

Caso não aceite valores númericos você deverá realizar um teste em que seu sistema não deverá aceitar um texto com um número e aí, para garantir a validação, os demais critérios de aceite deverão estar em conformidade com o esperado pelo sistema. Exemplo:

> O sistema aceita texto de tamanho fixo 5, sem caracteres especiais e sem números.

Para validar apenas a questão do número seu texto deverá ter tamanho 5 e não conter caracteres especiais. Exemplo

> Test1, 1Test, Te1st

Nesse caso são três testes para cada um dos valores e o sistema não deve aceitar esse tipo de texto. 

#### 3. Aceita caracteres especiais?

Caso não aceite caracteres especiais você deverá realizar diversos testes em que seu sistema não deverá aceitar um texto com nenhum tipo de caractere espceial, ou nenhum dos caracteres citados nos critérios de aceitação. Para garantir a validação, os demais critérios de aceite deverão estar em conformidade com o esperado pelo sistema. Exemplo:

> O sistema aceita texto de tamanho fixo 5, sem caracteres especiais como @, # e $, e sem números.

Para validar apenas a questão dos caracteres especiais o seu texto deverá ter tamanho 5 e não conter números. Exemplo

> @Test, #Test, $Test, Test@, Test#, Test$, Te@st, Te#st, Te$st

Nesse caso são nove testes disintos e o sistema não deve aceitar esse tipo de texto. 

> Observe que no caso 2 e 3, os valores foram dispostos no começo, meio e final, pois deve ser verificado se a validação está ocorrendo por todo o texto e não apenas em suas extremidades. 

#### 4. Aceita valores só em caixa alta ou caixa baixa?

Caso o sistema só aceite texto em caixa alta, você deverá realizar um teste em que seu sistema não deverá aceitar um texto com letras minúsculas. 

> TEsT

Caso o sistema só aceite texto em caixa baixa, você deverá realizar um teste em que seu sistema não deverá aceitar um texto com letras maiúsculas. 

> teSt

#### 5. Deve ser preenchido em um formato específico para aceitar o dado ou já é atribuida uma formatação ao inserir o dado?

##### Caso o sistema deva receber um texto em um determinado formato

Você deverá realizar diversos testes com o formato definido e fora do formato definido. Exemplo:

> Deve aceitar a data no formato: dd/mm 

Para validar você realizará o teste de sucesso, em que seu sistema aceita o formato inserido. Exemplo:

> 22/03 

E os testes de erro, em que seu sistema não aceita o formato inserido. Exemplo:

> 2203, 22-03, 22 03, 22\03, 22|03, ...

Aqui são diversas as opções possiveis, cabe a você avaliar quantos testes são necessários para garantir a validação do seus sistema.

##### Caso o sistema deva receber um texto e realizar a formatação automática

Nesse caso só é necessário realizar o teste passando os valores que devem ser recebidos e validar se a saída é a esperada da regra de formatação.
