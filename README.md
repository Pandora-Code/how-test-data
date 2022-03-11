<p align="center">
 <img width="200px" src="https://avatars.githubusercontent.com/u/87428056?s=200&v=4" align="center" alt="pandora-code" />
 <h2 align="center">Quais valores testar para cada tipo de dado?</h2>
 <p align="center">Vou apresentar para vocês quais valores devem ser usados para testar cada tipo de dado</p>
 <p align="center"> :warning: IN PROGRESS :warning: </p>
</p>

## Sobre

Na programação aprendemos que existem alguns tipos de dados básicos, que são: string, integer, float, boolean...

Aqui vamos trabalhar os tipos como os do mundo real, que nada mais são esses tipos básicos acima com regras especificas para eles.
Contudo, primeiro vamos entender um pouco sobre alguns conceitos em testes.

### Análise do Valor Limite

A `análise do valor limite` é uma técnica de teste utilizada para exercitar os limites do domínio de entrada. Então você sempre irá pegar um dado dentro do limite e um dado fora do limite. Contudo não pode ser qualquer dado, tem que ser o da extremidade do limite. 

Dado que L seja o limite, seus valores serão L-1 e L ou L e L+1, isso depende de onde está localizado o seu limite.

Exemplo:

> Nosso sistema só aceita pessoas maiores de idade.

Fique atento pois para cada países essa regra é distinta. Vamos pegar o Brasil como exemplo. No Brasil a maioridade é a partir dos 18 anos. O teste do valor limite para esse caso seria os valores:

> Teste 01: Uma pessoa com idade de 17 anos

> Teste 02: Uma pessoa com idade de 18 anos

Dado que com 17 anos não será aceito no sistema e 18 será aceito no sistema. Então nosso teste deverá seguir essa regra, no `Teste 01` o sistema não deverá cadastrar uma pessoa com 17 anos de idade. Já no `Teste 02` ele deverá cadastrar a pessoa.


## Tipos de dados

### Texto ou String

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

##### Caso o sistema deva receber um texto e realizar a formatação automatica

Nesse caso só é necessário realizar o teste passando os valores que devem ser recebidos e validar se a saída é a esperada da regra de formatação.
