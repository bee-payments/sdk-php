## Bee SDK PHP

É uma biblioteca desenvolvida para php com intuito de facilitar a conexão entre os desenvolvedores e a [Bee](https://bee.cash).    

A simplicidade é nosso lema, pois com poucas linhas de código você consegue transferir dinheiro para qualquer usuário cadastrado na [Bee](https://bee.cash).    

Veja como é simples fazer uma transferência:  

**1: Inclua a biblioteca**
```php
require 'src/bee.php';
```  

**2: Inicie a instância** 
```php
$bee = new Bee('seu-token');	
```  

**3: Crie uma tranferência**

```php
$bee->transfer([
   'username' => 'usuario-destino', // Usuário da Bee Pagamentos
   'amount' => 100, // Valor a ser transferido
   'coin' => 'brl', // Moeda que deseja transferir
]);
```  

Simples assim!  
Sua tranferência foi criada, veja abaixo o retornado desta solicitação.  

Campo | Tipo | Descrição
:----|:----|:---------
success | boolean  | **true** em caso de sucesso  **false** em caso de falha. |
errors | array | erros ocorridos durante a solicitação. este campo só existirá caso success seja **false**. |
result | array | array com os dados da transação. |

##### Confira a documentação completa [clicando aqui](https://github.com/bee-payments/sdk-php/blob/master/docs/pt.md).