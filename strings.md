## Exercício de strings
Faça um programa que leia uma string (pode estar numa variável para simplificar) e a modifique conforme as instruções abaixo, o primeiro caractere irá influenciar como os caracteres alfabéticos (letras) da string serão transformados, já o último caractere, como os caracteres numéricos da string serão transformados.

Sempre que o primeiro caractere da string for:
- `$` "Criptografa" todos os caracteres alfabéticos (a-z, A-Z), pulando 2 caracteres à frente (cíclico), por exemplo "A" se torna "C", "b" se torna "d", "K" se torna "M" e "Z" se torna "B".
- `^` Converte todos os caracteres alfabéticos em uppercase, a se torna A, z se torna Z, D continua D.
- `_` Converte todos os caracteres alfabéticos em lowercase, A se torna a, Z se torna z, d continua d.

Sempre que o último caractere da string for:
- `#` Converte cada caractere numérico (0-9) encontrado para o caractere 7
- `%` Converte cada caractere numérico para 0 caso ele seja par ou 1 caso ele seja ímpar
- `/` Converte cada caractere numérico para ele mesmo dividido pela metade arredondado para cima<br/>por exemplo: 2 => 1, 5 => 3, 7 => 4, 0 => 0

Exemplo de entrada - saída:
- 00000# -> 77777#
- $787878abc% -> $101010cde%
- ^no_ecziste_almuerzo_gratis -> ^NO_ECZISTE_ALMUERZO_GRATIS
- _Milton-012345-Friedman/ -> _milton-011223-friedman/

Dicas pra resolver o problema:
Resolve uma coisa de cada vez, faz funcionar os filtros de caractere primeiro, cria uma lógica pra  saber se é um caractere ou letra ou outro (se for outro, foda-se, não faz nada), daí vai testando conforme desenvolve e checando entradas que poderiam dar problema, com 0, sem 0, se atenta nas regras que tu tem que implementar, estuda sobre o que é o teu problema, lê sobre os caracteres e charcodes (no js, `"meu texto".charCodeAt(x)`), lê sobre o que é unicode, table ascii, tudo isso ai todo programador de verdade tem que saber de cor e salteado.

Material pra resolver o problema:<br/>
- [https://unicode-table.com/en](https://unicode-table.com/en)
- [https://unicode-table.com/en/blocks/basic-latin](https://unicode-table.com/en)
- Lê sobre tabela ascii 7bits em latim (começo da tabela unicode do 0 ao 127), todo desenvolvedor precisa saber como funciona uma string e os caracteres, e como que se usaria um caractere como um valor, porque é isso que ele é, um dado, na verdade todos os dados por mais complicadinho que são, é um monte de 0 e 1 no final das contas, se quiser ver mais como funciona, procura sobre UTF-8, UTF-16, etc. Toda a stack web é baseada em documentos, texto, strings e caracteres, então aprenda.

desafios:<br/>
Pode fazer enquanto desenvolve ou depois melhora tua solução pra bater com os desafios
1) Resolve o problema usando matemática, sem precisar fazendo ifs gigantescos, só usando o valor do caractere unicode, mapeia ele em outro, por exemplo se o caractere for == 90 (Z), e tu quer mapear ele pra B, vai se transformar em 66 (B), o valor 65 é o A, se tu seguir os link q eu mandei ou rodar uns código ai tu conclui isso, e que o "a" é 97 por exemplo, letras lowercase começam mais adiante na tabela.
2) Faz um for pra varrer a string de entrada uma vez só, não precisa ficar indo e voltando e transformando tudo de novo, e, o principal, tu não precisa varrer todo o array pra decidir se o primeiro caractere e o último é $ ou ^, tu pode checar isso só uma vez no começo, não precisa fazer if dentro do for pra ver isso, pra cada caractere, tu só precisa ver se é numérico, alfabético ou outro (que aí não faz nada, ou dá um "continue" no for). pra ti fazer isso, tu pode usar uma variável que aponta pra uma função, aí tu só faz um if no começo pra pegar essa função e salvar ela numa variável, por exemplo:

```js
let funcaoDosNumeros;
if (entrada[entrada.length-1] == "#") {
	// atribui uma funcao que retorna 7 sempre
	funcaoDosNumeros = () => 7;
}
```

Pra resolver o desafio 2, ler sobre: higher order function / first class function, closures, função que retorna uma função.
