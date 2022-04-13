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

### Campo de Texto
### Campo Númerico
### Campo Data
### Campo de Confirmação
### Email
### Senha
### CPF, CEP, CNPJ  
### Telefone
### Dados Bancários
