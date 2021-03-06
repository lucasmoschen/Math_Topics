# Monitorias 12 e 13

## Autovalores e Autovetores

**Definição:** Autovetor é um vetor ($\neq \vec{0}$) que tem como imagem
de uma transformação linear um vetor proporcional. A proporção é chamada
de autovalor.

**Polinômio Característico:** Polinômio cujas raízes são os autovalores
de uma transformação linear.

**Subespaço invariante:** Também conhecido como auto-espaço, é formado
pela combinação dos autovetores associados ao mesmo autovalor.

**Teorema 1:** Seja $A$ um operador linear, $\lambda$ um autovalor e
$v$ um autovetor. $Av = \lambda v \implies A^nv = \lambda^n v$.

**Teorema 2:** A autovalores diferentes do mesmo operador correspondem
autovetores linearmente independentes.

## Mudança de Base

Considere as seguintes bases:

$E = \{e_1, ..., e_n\}$

$U = \{u_1, ..., u_n\}$

$V = \{v_1,...,v_n\}$

Considere $w = (x_1,...,x_n)$. Isso significa que $w$ é escrito como uma
combinação linear dos vetores da base $E$, canônica, e os coeficientes
são $x_1, ..., x_n$. Imagine que queiramos escrever na base $U$. Para
isso, basta encontrarmos os coeficientes de cada vetor da base $U$. Para
isso, basta resolver o sistema linear onde cada vetor de $U$ é uma
coluna e o vetor restultado é o vetor na base canônica.

Assim, a matriz formada pelos vetores da base $U$ formam uma matriz que
transforma vetores da base $U$ em vetores da base canônica. A inversa
faz o processo contrário.

Se quiséssemos mudar da base $E$ para a base $U$ sem o uso da inversa,
só precisamos saber a transformação dos vetores da base canônica.

Para fazer a transformação de uma base em outra, basta transformarmos na
canônica como intermédio.

## Matrizes Semelhantes e Diagonalização

**Definição:** Duas matrizes são semelhantes se existe $P$ invertível
tal que $B = P^{-1}AP (AP = PB)$, que tem o mesmo polinômio
característico e o mesmo determinante.

**Diagonalização:** Uma matriz é diagonalizável se existe uma matriz
semelhante que seja diagonal. $A$ é diagonálizável se, e só se, tiver
$n$ autovetores LI. Nesse caso $P$ é a matriz cujas colunas são os
autovetores de $A$ e $D$ os autovalores correspontes.

Observe que $P^{-1}AP = D$, logo para transformar um vetor na base $V$
em outro na base $V$ correspondente a imagem desse vetor na base
canônica da matriz $A$, basta usar a transformação $D$.

## Recorrências

Podemos utilizar matrizes para representar recorrências. Um exemplo
famoso é a sequência de Fibonight.

## Produto Interno

Seja $E$ um espaço vetorial e $u, v \in E$. Define-se produto interno
com $<u,v>$ com um número real que satisfaz as seguintes condições:

-   $<u,v + v'> = <u,v> + <u,v'>$ e $<u + u',v> = <u,v> + <u',v>$

-   $<u,v> = <v,u>$

-   $<\alpha u,v> = \alpha<u,v>$ e $<u,\alpha v> = \alpha<u,v>$

-   Se $u \neq 0$, $<u,u> > 0$

## Projeções

Já sabemos que $p = (\frac{u\cdot v}{v\cdot v})v$ é a projeção do vetor
$u$ sobre a reta gerada por $v$. Quando queremos projetar um vetor $v$
sobre um hiperplano $\pi$, com vetor nornal $n$, temos que $v = p + tn$,
onde $t$ é uma constante. Logo, podemos montar um sistema com $n$
equações.

## Ortogonalidade

Se $<u,v> = 0$, dizemos que $u$ e $v$ são ortogonais. Um conjunto é dito
ortogonal se a cada par de vetores, eles são ortogonais. Ele será
ortonormal quando seus vetores ortogonais forem normalizados. Note que
se $X$ é um conjunto ortogonal, então é LI.

### Ortogonalização de Gram-Schimidt

Lembre-se: Defina um vetor inicial e utilize a ideia de que cada outro
vetor será subtraído das projeções do vetor calculado previamente.

### Projeção de um vetor sobre um subespaço

Seja $W$ um subespaço de $E$ e $\alpha$ uma base ortogonal desse
subespaço.

$p = proj_W v = \sum_{i=1}^n proj_{\alpha_i} v$

## Informações Adicionais

**Extendendo a ideia dos autovalores:** Dado um operador linear
$A: E \to E$ ou existe um vetor $u \in E$ tal que $Au = \lambda u$. Ou,
então, existem $u, v \in E$ linearmente independentes, tais que
$Au = \alpha u + \beta v$ e $Av = \gamma u + \delta v$.

**Invariante:** Diz-se que um subespaço vetorial $F \subset E$ é
invariante pelo operador $A: E \to F$ quando $A(F) \subset F$. Isto é,
quando a imagem dos vetorres desse subespaço estão nesse subespaço. Um
subespaço de dimensão 1 é invariante por $A$ se, e somente se, existe um
número $\lambda$ tal que $Av = \lambda v, \forall v \in F$. Se $u,v$
formam um subespaço de dimensão $2$, ele será invariante se, e só se,
$Au \in F$ e $Av \in F$.

**Teorema:** Todo operador linear num espaço vetorial de dimensão finita
possui um subespaço invariante de dimensão 1 ou 2. Para provar esse
teorema, temos que provar o lema que diz que existem um polinômio de
grau 1 ou 2 e um vetor $v$ tal que $p(A)\cdot v = 0$.

## Cadeias de Markov

**Definição:** É uma série temporal discreta no qual a distribuição de
uma população pode ser calculada por recorrência. Ad condições são que a
população nunca torna-se negativa e que a população total é fixa.
Podemos utilizar uma matriz de tranição que descreva a movimentação
probilística dessa população. Requere-se que a soma de cada coluna seja
1 e que não haja entradas negativas. O elemento $ij$ da matriz descreve
a probabilidade da população passar do estado $j$ para o estadp $i$. Se
$T$ possui alguma potêncua com todas as entradas positivas, é dito
regular. Uma matrzi de transição regular terá um estado estacionário.
$Ts = s$. É possível mostrar que qualquer matriz de transição com as
condições dadas deve ter um autovalor $1$.
