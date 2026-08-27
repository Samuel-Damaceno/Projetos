# Lista de Exercícios Sequenciais — Lista 03

## Introdução

Este documento reúne as soluções dos exercícios da **Lista de Exercícios Sequenciais — Lista 03**, utilizando **Portugol/Visualg**.

Os exercícios trabalham principalmente com:
- entrada de dados;
- cálculos aritméticos;
- conversão de unidades;
- cálculo de totais e médias;
- apresentação dos resultados.

As explicações aparecem antes de cada algoritmo para facilitar o entendimento da lógica utilizada.

---

# Exercício 1 — Feira da Madalena

## Explicação

Madalena comprou **laranjas, verduras e queijo**. Para cada produto, o programa recebe a quantidade comprada e o preço unitário.

Primeiro, calculamos o valor gasto com cada produto:

**valor do produto = quantidade × preço**

Depois, somamos os três valores para obter o **total geral gasto**.

Por fim, calculamos a **média aritmética dos valores dos três produtos**:

**média = total geral ÷ 3**

## Algoritmo

```portugol
algoritmo "Exercicio_1"

var
   qtdLaranjas, qtdVerduras, qtdQueijo: inteiro
   precoLaranja, precoVerdura, precoQueijo: real
   totalLaranjas, totalVerduras, totalQueijo: real
   totalGeral, media: real

inicio

   escreva("Quantidade de laranjas: ")
   leia(qtdLaranjas)
   escreva("Preco da laranja: R$ ")
   leia(precoLaranja)

   escreva("Quantidade de verduras: ")
   leia(qtdVerduras)
   escreva("Preco da verdura: R$ ")
   leia(precoVerdura)

   escreva("Quantidade de queijos: ")
   leia(qtdQueijo)
   escreva("Preco do queijo: R$ ")
   leia(precoQueijo)

   totalLaranjas <- qtdLaranjas * precoLaranja
   totalVerduras <- qtdVerduras * precoVerdura
   totalQueijo <- qtdQueijo * precoQueijo

   totalGeral <- totalLaranjas + totalVerduras + totalQueijo
   media <- totalGeral / 3

   escreval("Total das laranjas: R$ ", totalLaranjas:5:2)
   escreval("Total das verduras: R$ ", totalVerduras:5:2)
   escreval("Total dos queijos: R$ ", totalQueijo:5:2)
   escreval("Total geral gasto: R$ ", totalGeral:5:2)
   escreval("Media aritmetica: R$ ", media:5:2)

fimalgoritmo
```

---

# Exercício 2 — Hidratação dos competidores

## Explicação

O enunciado informa que existem **4 hidratações** e que os copos possuem volumes de **350 ml, 430 ml e 510 ml**.

Como o exercício pede a quantidade de água consumida por **4 competidores**, o programa recebe, para cada competidor, a quantidade de copos consumidos e o volume de cada copo.

A quantidade de água consumida por cada competidor é calculada por:

**consumo = quantidade de copos × volume do copo**

Depois, somamos o consumo dos quatro competidores para encontrar o **total de água consumida**.

A média é:

**média = total consumido ÷ 4**

> **Observação:** há uma pequena inconsistência no enunciado da imagem: ele menciona inicialmente três competidores, mas posteriormente solicita os cálculos para quatro. A solução abaixo considera quatro competidores, conforme solicitado nos resultados.

## Algoritmo

```portugol
algoritmo "Exercicio_2"

var
   copos1, copos2, copos3, copos4: inteiro
   volume1, volume2, volume3, volume4: real
   consumo1, consumo2, consumo3, consumo4: real
   total, media: real

inicio

   escreva("Quantidade de copos do competidor 1: ")
   leia(copos1)
   escreva("Volume de cada copo do competidor 1 (ml): ")
   leia(volume1)

   escreva("Quantidade de copos do competidor 2: ")
   leia(copos2)
   escreva("Volume de cada copo do competidor 2 (ml): ")
   leia(volume2)

   escreva("Quantidade de copos do competidor 3: ")
   leia(copos3)
   escreva("Volume de cada copo do competidor 3 (ml): ")
   leia(volume3)

   escreva("Quantidade de copos do competidor 4: ")
   leia(copos4)
   escreva("Volume de cada copo do competidor 4 (ml): ")
   leia(volume4)

   consumo1 <- copos1 * volume1
   consumo2 <- copos2 * volume2
   consumo3 <- copos3 * volume3
   consumo4 <- copos4 * volume4

   total <- consumo1 + consumo2 + consumo3 + consumo4
   media <- total / 4

   escreval("Agua consumida pelo competidor 1: ", consumo1:5:2, " ml")
   escreval("Agua consumida pelo competidor 2: ", consumo2:5:2, " ml")
   escreval("Agua consumida pelo competidor 3: ", consumo3:5:2, " ml")
   escreval("Agua consumida pelo competidor 4: ", consumo4:5:2, " ml")
   escreval("Total consumido pelos 4: ", total:5:2, " ml")
   escreval("Media consumida: ", media:5:2, " ml")

fimalgoritmo
```

---

# Exercício 3 — Restaurante COMIDA DA BOA

## Explicação

O restaurante cobra **R$ 36,00 por quilograma** dos alimentos gerais/diversos e **R$ 60,00 por quilograma** da carne.

Como o enunciado solicita que o peso seja informado em **gramas**, precisamos converter os valores para quilogramas:

**quilogramas = gramas ÷ 1000**

Depois calculamos separadamente:

**valor dos alimentos diversos = peso em kg × 36**

**valor da carne = peso da carne em kg × 60**

Somando os dois valores, encontramos o **total da conta**.

Também somamos os pesos para descobrir o **peso total da marmita**.

## Algoritmo

```portugol
algoritmo "Exercicio_3"

var
   pesoDiversos, pesoCarne: real
   pesoDiversosKg, pesoCarneKg: real
   valorDiversos, valorCarne, valorTotal: real
   pesoTotal: real

inicio

   escreva("Peso dos alimentos diversos (gramas): ")
   leia(pesoDiversos)

   escreva("Peso da carne (gramas): ")
   leia(pesoCarne)

   pesoDiversosKg <- pesoDiversos / 1000
   pesoCarneKg <- pesoCarne / 1000

   valorDiversos <- pesoDiversosKg * 36
   valorCarne <- pesoCarneKg * 60

   valorTotal <- valorDiversos + valorCarne
   pesoTotal <- pesoDiversos + pesoCarne

   escreval("Valor dos alimentos diversos: R$ ", valorDiversos:5:2)
   escreval("Valor da carne: R$ ", valorCarne:5:2)
   escreval("Valor total da conta: R$ ", valorTotal:5:2)
   escreval("Peso total da marmita: ", pesoTotal:5:2, " gramas")

fimalgoritmo
```

---

# Exercício 4 — Corrida dos automóveis

## Explicação

Três automóveis participam de uma corrida de **380 km** e fazem **3 paradas para abastecimento**.

Para cada carro, o programa recebe a quantidade de litros colocada em cada uma das três paradas e a quantidade de combustível que restou no final.

Primeiro, somamos os três abastecimentos:

**total abastecido = parada 1 + parada 2 + parada 3**

Depois calculamos o combustível consumido:

**combustível consumido = total abastecido − combustível restante**

Para calcular o consumo médio por quilômetro:

**consumo médio = litros consumidos ÷ 380**

O limite do tanque é de 40 litros, mas como o enunciado não pede uma verificação de limite e este é um exercício sequencial, não é necessário utilizar uma estrutura condicional.

## Algoritmo

```portugol
algoritmo "Exercicio_4"

var
   carro1p1, carro1p2, carro1p3: real
   carro2p1, carro2p2, carro2p3: real
   carro3p1, carro3p2, carro3p3: real

   resto1, resto2, resto3: real
   total1, total2, total3: real
   consumo1, consumo2, consumo3: real
   media1, media2, media3: real

inicio

   escreval("=== CARRO 1 ===")
   escreva("Litros na parada 1: ")
   leia(carro1p1)
   escreva("Litros na parada 2: ")
   leia(carro1p2)
   escreva("Litros na parada 3: ")
   leia(carro1p3)
   escreva("Litros restantes no final: ")
   leia(resto1)

   escreval("=== CARRO 2 ===")
   escreva("Litros na parada 1: ")
   leia(carro2p1)
   escreva("Litros na parada 2: ")
   leia(carro2p2)
   escreva("Litros na parada 3: ")
   leia(carro2p3)
   escreva("Litros restantes no final: ")
   leia(resto2)

   escreval("=== CARRO 3 ===")
   escreva("Litros na parada 1: ")
   leia(carro3p1)
   escreva("Litros na parada 2: ")
   leia(carro3p2)
   escreva("Litros na parada 3: ")
   leia(carro3p3)
   escreva("Litros restantes no final: ")
   leia(resto3)

   total1 <- carro1p1 + carro1p2 + carro1p3
   total2 <- carro2p1 + carro2p2 + carro2p3
   total3 <- carro3p1 + carro3p2 + carro3p3

   consumo1 <- total1 - resto1
   consumo2 <- total2 - resto2
   consumo3 <- total3 - resto3

   media1 <- consumo1 / 380
   media2 <- consumo2 / 380
   media3 <- consumo3 / 380

   escreval(" ")
   escreval("=== RESULTADOS ===")

   escreval("Total colocado no carro 1: ", total1:5:2, " litros")
   escreval("Total consumido pelo carro 1: ", consumo1:5:2, " litros")
   escreval("Consumo medio do carro 1: ", media1:5:4, " litros/km")

   escreval("Total colocado no carro 2: ", total2:5:2, " litros")
   escreval("Total consumido pelo carro 2: ", consumo2:5:2, " litros")
   escreval("Consumo medio do carro 2: ", media2:5:4, " litros/km")

   escreval("Total colocado no carro 3: ", total3:5:2, " litros")
   escreval("Total consumido pelo carro 3: ", consumo3:5:2, " litros")
   escreval("Consumo medio do carro 3: ", media3:5:4, " litros/km")

fimalgoritmo
```

---

# Exercício 5 — Compra de limão, maçã e tomate

## Explicação

Neste exercício, são comprados **limão, maçã e tomate**.

Para cada produto, o programa recebe:
- quantidade;
- preço;
- peso.

O gasto com cada produto é calculado multiplicando a quantidade pelo preço.

Depois, somamos os gastos para obter o **total geral da compra**.

O peso total é a soma dos pesos dos três produtos.

Por fim, calculamos o preço médio considerando os três produtos:

**preço médio = total gasto ÷ 3**

## Algoritmo

```portugol
algoritmo "Exercicio_5"

var
   qtdLimao, qtdMaca, qtdTomate: real
   precoLimao, precoMaca, precoTomate: real
   pesoLimao, pesoMaca, pesoTomate: real
   gastoLimao, gastoMaca, gastoTomate: real
   totalGasto, pesoTotal, precoMedio: real

inicio

   escreva("Quantidade de limoes: ")
   leia(qtdLimao)
   escreva("Preco dos limoes: R$ ")
   leia(precoLimao)
   escreva("Peso dos limoes (kg): ")
   leia(pesoLimao)

   escreva("Quantidade de macas: ")
   leia(qtdMaca)
   escreva("Preco das macas: R$ ")
   leia(precoMaca)
   escreva("Peso das macas (kg): ")
   leia(pesoMaca)

   escreva("Quantidade de tomates: ")
   leia(qtdTomate)
   escreva("Preco dos tomates: R$ ")
   leia(precoTomate)
   escreva("Peso dos tomates (kg): ")
   leia(pesoTomate)

   gastoLimao <- qtdLimao * precoLimao
   gastoMaca <- qtdMaca * precoMaca
   gastoTomate <- qtdTomate * precoTomate

   totalGasto <- gastoLimao + gastoMaca + gastoTomate
   pesoTotal <- pesoLimao + pesoMaca + pesoTomate
   precoMedio <- totalGasto / 3

   escreval("Total gasto: R$ ", totalGasto:5:2)
   escreval("Peso total da compra: ", pesoTotal:5:2, " kg")
   escreval("Preco medio dos produtos: R$ ", precoMedio:5:2)

fimalgoritmo
```

---

# Exercício 6 — Compra das quatro novilhas

## Explicação

O fazendeiro comprou **4 novilhas** com pesos variados.

O peso é informado em **arrobas**, sendo que:

**1 arroba = 15 kg**

O preço de cada novilha depende do preço da arroba. Portanto, o programa recebe o peso em arrobas e o preço da arroba para cada animal.

O gasto de cada novilha é:

**valor = arrobas × preço da arroba**

Para descobrir o peso em quilogramas:

**kg = arrobas × 15**

Depois somamos os valores para obter o **total gasto**, somamos as arrobas e os quilogramas para obter os pesos totais e calculamos o **preço médio das quatro novilhas**.

## Algoritmo

```portugol
algoritmo "Exercicio_6"

var
   arroba1, arroba2, arroba3, arroba4: real
   preco1, preco2, preco3, preco4: real
   kg1, kg2, kg3, kg4: real
   gasto1, gasto2, gasto3, gasto4: real
   totalGasto, totalArrobas, totalKg, precoMedio: real

inicio

   escreval("=== NOVILHA 1 ===")
   escreva("Peso em arrobas: ")
   leia(arroba1)
   escreva("Preco por arroba: R$ ")
   leia(preco1)

   escreval("=== NOVILHA 2 ===")
   escreva("Peso em arrobas: ")
   leia(arroba2)
   escreva("Preco por arroba: R$ ")
   leia(preco2)

   escreval("=== NOVILHA 3 ===")
   escreva("Peso em arrobas: ")
   leia(arroba3)
   escreva("Preco por arroba: R$ ")
   leia(preco3)

   escreval("=== NOVILHA 4 ===")
   escreva("Peso em arrobas: ")
   leia(arroba4)
   escreva("Preco por arroba: R$ ")
   leia(preco4)

   gasto1 <- arroba1 * preco1
   gasto2 <- arroba2 * preco2
   gasto3 <- arroba3 * preco3
   gasto4 <- arroba4 * preco4

   kg1 <- arroba1 * 15
   kg2 <- arroba2 * 15
   kg3 <- arroba3 * 15
   kg4 <- arroba4 * 15

   totalGasto <- gasto1 + gasto2 + gasto3 + gasto4
   totalArrobas <- arroba1 + arroba2 + arroba3 + arroba4
   totalKg <- kg1 + kg2 + kg3 + kg4
   precoMedio <- totalGasto / 4

   escreval(" ")
   escreval("Total gasto com as novilhas: R$ ", totalGasto:5:2)
   escreval("Total em arrobas: ", totalArrobas:5:2)
   escreval("Total em quilogramas: ", totalKg:5:2, " kg")
   escreval("Preco medio das novilhas: R$ ", precoMedio:5:2)

fimalgoritmo
```

---

# Exercício 7 — Jogo Calouros x Queimados

## Explicação

Neste exercício, temos um jogo de futebol entre os times **Calouros** e **Queimados**.

O enunciado informa que foram marcados:
- 7 gols no primeiro tempo;
- 4 gols no segundo tempo.

Para determinar quantos gols cada equipe marcou, o programa recebe os gols de cada time em cada tempo.

O total de gols de cada equipe é calculado somando os gols do primeiro e do segundo tempo:

**gols finais = gols do primeiro tempo + gols do segundo tempo**

Depois, mostramos o placar final.

## Algoritmo

```portugol
algoritmo "Exercicio_7"

var
   calouros1, queimados1: inteiro
   calouros2, queimados2: inteiro
   totalCalouros, totalQueimados: inteiro
   totalPrimeiro, totalSegundo: inteiro

inicio

   escreva("Gols dos Calouros no primeiro tempo: ")
   leia(calouros1)

   escreva("Gols dos Queimados no primeiro tempo: ")
   leia(queimados1)

   escreva("Gols dos Calouros no segundo tempo: ")
   leia(calouros2)

   escreva("Gols dos Queimados no segundo tempo: ")
   leia(queimados2)

   totalPrimeiro <- calouros1 + queimados1
   totalSegundo <- calouros2 + queimados2

   totalCalouros <- calouros1 + calouros2
   totalQueimados <- queimados1 + queimados2

   escreval(" ")
   escreval("Gols dos Calouros no primeiro tempo: ", calouros1)
   escreval("Gols dos Queimados no primeiro tempo: ", queimados1)
   escreval("Gols dos Calouros no segundo tempo: ", calouros2)
   escreval("Gols dos Queimados no segundo tempo: ", queimados2)

   escreval(" ")
   escreval("Placar final:")
   escreval("Calouros ", totalCalouros, " x ", totalQueimados, " Queimados")

fimalgoritmo
```

---

# Exercício 8

## Explicação

Na imagem enviada, o exercício 8 aparece apenas como **“x”**, sem um enunciado completo.

Por isso, não existem informações suficientes para montar o algoritmo ou saber qual cálculo deve ser realizado.

Assim que o enunciado completo do exercício 8 estiver disponível, ele poderá ser acrescentado ao documento.

---

# Fórmulas utilizadas

## Exercício 1
**Total do produto = quantidade × preço**

**Média = total geral ÷ 3**

## Exercício 2
**Água consumida = quantidade de copos × volume do copo**

**Média = total de água ÷ 4**

## Exercício 3
**Kg = gramas ÷ 1000**

**Valor dos alimentos = peso em kg × R$ 36,00**

**Valor da carne = peso em kg × R$ 60,00**

## Exercício 4
**Total abastecido = parada 1 + parada 2 + parada 3**

**Combustível consumido = total abastecido − combustível restante**

**Consumo médio = litros consumidos ÷ 380**

## Exercício 5
**Gasto = quantidade × preço**

**Peso total = peso do limão + peso da maçã + peso do tomate**

**Preço médio = total gasto ÷ 3**

## Exercício 6
**1 arroba = 15 kg**

**Peso em kg = arrobas × 15**

**Valor da novilha = arrobas × preço da arroba**

**Preço médio = total gasto ÷ 4**

## Exercício 7
**Gols finais = gols do primeiro tempo + gols do segundo tempo**
