# Algoritmo de Tabuada Criado em Portugol :computer: :keyboard:

## FLuxograma da Tabuada

```flow
st=>start: Start
op1=>operation: Inteiro contador, limite, valor, resultado
op2=>operation: contador = 0
op3=>operation: limite = 10
io1=>inputoutput: Digite qual tabuada você quer ver, escolha valores entre 1 e 10.
io2=>inputoutput: Entrada valor
cond1=>condition: valor <= 10
op4=>operation: Você deve digitar um valor entre 1 e 10!
cond2=>condition: valor > 0
op5=>operation: Você deve digitar um valor entre 1 e 10!
op6=>operation: Estrutura de Repetição. contador<=limite
op7=>operation: resultado=valor*contador
io3=>inputoutput: valor + " x " & contador + " = " + resultado
op8=>operation: contador++
e=>end

st->op1->op2->op3->io1->io2->cond1
cond1(yes)->cond2
cond2(yes)->op6->op7->io3->op8->cond2
cond2(no)->op5->e
cond1(no)->op4->e

```

## Código em Portugol



`programa`
`{`
	`faca`
	`{`
	`funcao inicio()`
	`{`
		`inteiro contador, limite, valor, resultado // Declaração das variáveis`
		`contador = 0 // Contador para a estrutura de repetição`
		`limite = 20 // Limite, serve para definir a quantidade de operações que a estrutura de repetição realizará.`
		`escreva("Digite qual tabuada você quer ver, escolha valores entre 1 e 10! ")`
		`leia(valor) // Entrada para a variável valor, que é responsável pela definição da tabuada e imposição do domínio do algoritmo.`
		`se (valor<=10) {  // Limitando a tabuada para valores menores ou iguais a 10`
			`se (valor>0) { // Limitando a tabuada para valores entre 0 e 10`
				`faca { // Estrutura de repetição que realiza os cálculos, imprime os resultados e modifica o contador`
					`resultado = valor * contador`
					`escreva(valor + " x " + contador + " = " + resultado + "\n")`
					`contador++`
				`}enquanto (contador<=limite)`
			`}`
			`senao { // Caso o valor introduzido não esteja dentro do domínio deste algoritmo`
				`escreva("Você deve escolher valores entre 1 e 10! ")`
			`}`
		`} senao { // Caso o valor introduzido não esteja dentro do domínio deste algoritmo`
			`escreva("Você deve escolher valores entre 1 e 10! ")`
	`}`
	`}`
	`} enquanto verdadeiro`
`}`

