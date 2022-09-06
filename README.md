# Vetores / Arrays

Os vetores, ou arrays, são estruturas que nos permitem armazenar uma lista de dados na memória do computador.
**Exemplos:** Lista de compras, alunos de uma turma, etc.

Para recuperar os itens de uma lista, utilizamos os vetores, indicando, numericamente, qual a posição do item que desejamos recuperar.

*Importante: Lembre que a primeira posição da lista corresponde com o número **0**, conforme representado na tabela abaixo .*

| Posição | Produto |
| :---: | :--- |
| 0 | Acerola |
| 1 | Banana |
| 2 | Laranja |
| 3 | Melancia |

***Guarde esta tabela como referência para os exemplos seguintes.***

Para armazenar os dados descritos acima em um array, usando JavaScript (JS), é necessário o seguinte código:
```javascript
const listaCompras = ["Acerola", "Banana", "Laranja", "Melancia"];
```
Para recuperar o conteúdo da primeira posição da lista, é necessário o seguinte código:
```javascript
listaCompras[0];
```
O conteúdo retornado será **"Acerola"**.

Já para recuperar o conteúdo da segunda posição da lista, o código será:
```javascript
listaCompras[1];
```
O conteúdo retornado será, portanto, **"Banana"**.

## Métodos para manipulação de Arrays
| Método | Utilidade |
| :--- | :--- |
| push() | Adiciona um elemento ao final do array. |
| pop() | Remove o último elemento ao final do array. |
| shift() | Remove o primeiro elemento do vetor e desloca os seguintes para cima. |
| unshift() | Adiciona um elemento no início do array e desloca os elementos para uma posição abaixo. |

Portanto, o código para adicionar um item (tanto ao fim - *push()* - quanto no início - *unshift()* - do array), será, respectivamente:
```javascript
listaCompras.push("Melão");
listaCompras.unshift("Abacaxi");
```

Já para remover um item (tanto ao fim - *pop()* - quanto no início - *shift()* - do array), será, respectivamente:
```javascript
listaCompras.pop();
listaCompras.shift();
```

Podemos também atribuir o valor de uma posição do array para uma const/let/var, usando o seguinte comando:
```javascript
const primeiroItem = listaCompras[0];
```
Considerando os itens descritos na Tabela, o conteúdo da const primeiroItem será **"Acerola"**.

Também existem alguns outros métodos que podem ser utilizados, tais quais:
| Método | Utilidade |
| :--- | :--- |
| splice() | Possibilita *emendar* o array. Utilizam-se parâmetros junto do método. |
| slice() | Tem por função *fatiar* o array. Também são necessários parâmetros para sua utilização. |

Imagine os seguintes exemplos:

* *const* **listaCompras** = ["Acerola", "Banana", "Laranja", "Melancia"];
* *const* **itensFim** = listaCompras.slice(-2);
  * Armazenará os dois últimos itens: **itensFim** terá os itens ["Laranja", "Melancia"]
* *const* **itensInicio** = listaCompras.slice(0, -1);
  * Armazenará todos os itens, com exceção do último: **itensInicio** terá os itens ["Acerola", "Banana", "Laranja"]
* *const* **itemRemovido** = listaCompras.splice(2, 1);
  * A partir do terceiro item da lista (correspondente com o número 2 do método splice), retirará um item (correspondente com o número 1 do método splice). Portanto, **itemRemovido** terá o conteúdo ["Laranja"], enquanto que o array original, **listaCompras**, será atualizado para ["Acerola", "Banana", "Melancia"];

Para ordenar os elementos do array, existem métodos que ordenam os itens de forma crescente e de forma decrescente.

***Após ordenar, não será possível retornar para a sequência anterior.***

| Método | Utilidade |
| :--- | :--- |
| sort() | Ordena os itens de forma crescente - do menor para o maior: **A->Z**. |
| reverse() | Ordena os itens de forma descrescente - do maior para o menor:  **Z->A**. |


## Propriedades dos Arrays

Existem propriedades que podem ser acessadas após a criação dos arrays. Uma das mais importantes é a propriedade que retorna a quantidade de elementos do array (tamanho), que é a propriedade *length*.
Ou seja, considerando o nosso array:

```javascript
const listaCompras = ["Acerola", "Banana", "Laranja", "Melancia"];
```

Ao executarmos o comando:
```javascript
listaCompras.length;
```
O conteúdo que retornará será **4**, que corresponde aos elementos que contém - que são as quatro frutas.

Alguns comandos úteis para retornar os dados do array em uma string (texto), são os:
```javascript
listaCompras.join();
```
O retorno será o seguinte:

**Acerola,Banana,Laranja,Melancia**

É possível passarmos um parâmetro ao usar o método **join()**, como no exemplo abaixo:
```javascript
listaCompras.join(" - ");
```
Ou seja, adicionamos ***espaço + hífen + espaço*** entre cada elemento do array para formar a string/texto de retorno, que será:
**Acerola - Banana - Laranja - Melancia**

*Também há o método toString() - listaCompras.toString() - porém não há possibilidade de customizar o retorno, estando sempre os itens separados por vírgula (Acerola,Banana,Laranja,Melancia).*

### Soletrando
Você sabia que também dá para soletrar um texto usando JS?

Existe o método Array.from(texto) que separa as letras de uma string. Veja o código abaixo:
```javascript
Array.from("Soletrando");
```
Ao executar esta instrução, o retorno será:

**["S", "o", "l", "e", "t", "r", "a", "n", "d", "o"]**

Ou seja, ele cria um array contendo todas as letras do parâmetro enviado para o método **from()**;