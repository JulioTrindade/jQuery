# DeviceJS

Júlio Cesar Trindade: 20161011110018 / GitHub Nickname: JulioTrindade;<br/>
Wesley Giovane: 20141011110166 / GitHub Nickname:WesleyGiovane;<br/>
Júlio Cesar Fernandes: 20141011110344 / GitHub Nickname: jcesar732;<br/>
Linguagem: DeviceJS

## Resumo

**Propósito da linguagem:** 

O DeviceJS tem como objetivo permitir que desenvolvedores familiarizados com bibliotecas de desenvolvimento da Web apliquem algo que aconteça dinamicamente no mundo físico.

**Paradgima da linguagem:** 

Procedural, visto que segue o conceito de um estado e de ações que manipulam esse estado, nele encontramos procedimentos que servem de mecanismos de estruturação. Podemos denominá-lo procedural por incluir procedimentos para estruturação.

**Data de criação:**
dd de mês de 2015

**Principal mantenedor**: 
- KeystoneJS

## Instalação e uso

**Como instalar?**
- O DeviceJS é um sistema distribuído;
- O DeviceJS pode distribuir um script em qualquer retransmissão capaz de executar o DeviceJS run-time;
- Execute o comando a seguir na linha de comando:
```js
  $ npm install devicejs
```
**Como usar?**
- Pode ser usado: em um banco de dados JSON distribuído em tempo real, que atualiza diretamente para o tempo de execução do DeviceJS. Em API baseada em objetos, baseada basicamente em base2 e Prototype. Em ganchos de serviço para drivers de dispositivo nativos para protocolos como: 6loWPAN, Z-Wave e ZigBee. Em um Catálogo que permite que dispositivos de todos os tipos sejam categorizados e cruzados em uma variedade de maneiras, e em APIs para lidar com JavaScript complexo, assíncrono, semelhante no conceito de  async.js.
- Execução: Os scripts e aplicativos escritos para DeviceJS podem executar e consequentemente controlar dispositivos em muitos locais. 
   
**Comandos:**
   
**Seletores:**
- Transformar toda a iluminação em um local para vermelho:
```js
  dev$.byLocation("kitchen").setColor("red");
```
- Mudar todos os dispositivos marcados como uma "luz" para desligado:
```js
  dev$.byTag('light').setOff();
```
**Eventos:**
- Pop-up de alerta de caixa de diálogo em um 'clique':
```js
  dev$.byDeviceAlias('hallway-sensor').trigger('motion',function(){dev$.byLocation('hallway').setOn();});
```
- Sensor de movimento acionado de acordo com a movimentação no ambiente:
```js
  function func1(){dev$.byTag('light').setOn();}dev$.trigger('motion', func1);
```
## Sintaxe básica

**Variáveis e constantes:**
Como o devicejs é uma linguagem que deriva do javascript, suas sintaxes são semelhantes
- Variáveis: Podem ser declaradas de 3 formas
```js
  var x = 42;
```
Apenas variáveis globais:
```js
  x = 34;
```
Para declarar uma variável local de escopo de bloco:
```js
  let z = 92;
```
- Constantes: 
```js
  const a = 3;
```
A constante não altera seu valor:
```js
  const a = 3;
  a = 10
  console.log(a); //retorno: 3
```

- Operadores relacionais:
'<': Menor que, '>': Maior que, '<=': Menor ou igual, '>=': Maior ou igual, '==': Igual, '!=': Diferente (não igual).

- Operadores lógicos:
AND (&&), OR (||) e NOT (!).

- Operadores aritméticos:
Operadores aritméticos tomam valores numéricos (sejam literais ou variáveis) como seus operandos e retornam um único valor númerico. Os operadores aritméticos padrão são os de soma (+), subtração (-), multiplicação (*) e divisão (/). Além desses que são comuns a outras linguagens de programação, o devicejs disponibiliza as operações de: resto da divisão (%), Incremento (++), Decremento (--), Negação (-), Adição (+) e exponenciação (**).

- Estruturas de controle condicional:
  - Use ''if' para especificar um bloco de código a ser executado, se uma condição especificada for verdadeira
  - Use 'else' para especificar um bloco de código a ser executado, se a mesma condição for falsa
  - Use 'else if' para especificar uma nova condição para testar, se a primeira condição for falsa
  - Use 'switch' para especificar muitos blocos alternativos de código a serem executados

- Estruturas de repetição:
  - 'for' : Repetições através de um bloco de código com um número determinado de vezes;
  - 'for / in' : Repetições através das propriedades de um objeto;
  - 'while' : passa por um bloco de código enquanto uma condição especificada for verdadeira;
  - 'Do / while' : também executa repetidamente através de um bloco de código enquanto uma condição especificada é verdadeira.

- Vetores, matrizes e strings:
  - Vetores: 
```js
  var frutas = ["Melancia", "Melão", "Goiaba"];
```
  - Matrizes: O devicejs não suporta a criação de matrizes, mas podem ser feitos vetores de vetores.
  - strings: 
  ```js
  var nomeMateria = "POS";
```
- Funções:
  - Uma função JavaScript é um bloco de código projetado para executar uma tarefa específica. 
  - Uma função JavaScript é executada quando "algo" a chama.
- Exemplo: 
```js
  function multiplica(num1, num2) {
    return num1 * num2; // a função retorna o produto de num1 e num2
  }
```
## Sintaxe OO
```js
class Quadrado extends Poligono {
  constructor(comprimento) {
    // super chama o construtor da classe pai que vai atribuir comprimento para
    // os atributos comprimento e altura herdados pela nossa classe filha Quadrado  
    super(comprimento, comprimento);
    // Nas classes filhas, super() deve ser chamado antes de usar o this. Sem ele 
    // vai ocorrer um erro de referência. O this agora se refere a classe filha Quadrado
    this.nome = 'Quadrado';
  }

  // os atributos a seguir são herdados da classe pai Poligono: altura, comprimento e area.

  get area() {
    return this.altura * this.comprimento;
  }

  set area(valor) {
    this.area = valor;
  } 
}
```
```js
- Classe
Define as características do objeto. Uma classe é uma definição modelo das propriedades e métodos de um objeto.
Objeto
Um exemplar de uma classe.
Atributo
Uma característica do objeto, como cor, modelo, fabricante se estivemos representando um veículo, por exemplo.
Método
Uma ação do objeto, como ligar, desligar, frear se estivemos representando um veículo, por exemplo. É uma subrotina ou função associada a uma classe.
Construtor
Um método chamado assim que um novo exemplar do objeto for criado. Ele geralmente tem o mesmo nome da classe que o contém.
Herança
Uma classe pode herdar características de outra classe.
Encapsulamento
Uma maneira de agrupar os dados e os métodos que usam os dados.
Abstração
A conjunção de herança complexa, métodos, propriedades de um objeto devem refletir adequadamente um modelo da realidade.
Polimorfismo
Diferentes classes podem definir o mesmo método ou propriedade.
