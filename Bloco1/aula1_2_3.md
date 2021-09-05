# Primeiro Bloco de teoria- Sistemas Evolutivos Aplicados a Robotica (SC0713)

* gitlab: https://gitlab.com/simoesusp/disciplinas/-/tree/master/SSC0713-Sistemas-Evolutivos-Aplicados-a-Robotica

## Aula 1:

* Gravação: https://drive.google.com/file/d/1z0wHTwafRw7nwQTY3KkOe3I3OxQAmEqq/view

### Procedimento de criação de um algoritmo evolutivo

1. Inicializar uma população

2. Avaliação (mais adaptado => maior nota (fitness))

3. Seleção (maior nota => maior probabilidade de ser selecinado)

4. Crossover

5. Mutação

6. Rearranjo da população

> Exemplo

1. Iniciar uma população com 10 individuos, associando cada individuo com um "cromossomo" (conjunto de parametros organizados em um vetor)
    * digmaos que queremos fazer café, para isso nosso vetor de parametros sera
    * Cafe => (Agua, Cafe, Acucar, leite), cada individuo da populacao tera uma certta quantidade de cada elemento:
i0 = (10, 3, 5, 10)
...
i9 = (8, 2, 6, 88)

2. Dar uma nota para cada individuo, sem segredo

3. O método que o simões mais gosta: Elitismo (melhor cruza com todos)
    * **NUNCA MATAR O MELHOR DE TODOS**

4. Cruzar (normalmente é só a media, porem há varios metodos)
(10, 3, 5, 10)
    x
(8, 2, 6, 88)
= (9, 2.5, 6.5, 49)

5. Mutacao: Sorteia alguns genes e soma (ou subtrai) uma TAXA DE MUTAÇÃO

6. Mata alguns individuos e substitui pelos filhos gerados

## Aula 2:

* Gravação: https://drive.google.com/file/d/1Fs3FRpP9Lc7Xapo_hsEGUy2lUowoZhnA/view?usp=sharing

> Foi aula particular pro Lucas Alves, mas tinha algumas informações interessantes. Entre elas: 

* Utilizar uma taxa de mutação variável

* Não utilizar a taxa de mutação como proporcao do valor do individuo

* Em um problema de procurar o max global de uma funcao toda torta, o algoritmo vai apidamente achar um maxmimo local e estabilizar. As mutações ao longo do tempo vao jogando individuos para longe até que alguma desça o vale e suba ate outro maximo local maior, ou até o max global (por isso taxas de mutaçoes pequenas podem inviabilizar esse processo e demorar mto tempo). Nesse exemplo uma taxa de mutação que ao ver o sistema estabilizar AUMENTASSE seria muito util para achar possiveis maximos maiores mais rapido 

## Aula 3:

* Gravação: https://drive.google.com/file/d/1uQqhGOfT46z6nad3q2lEvz49gr2bH9e1/view

> Aula meio aleatoria, porém continuamos a anotar os pontos principais

* Ao contrário da aula 2 onde o professor propos utilziar uma taxa de mutação que aumenta quando o sistema estabiliza, ele propos o exemplo de um braço robótico articulado que quer que sua ponta encoste em um ponto especifico. Nele seria interessante DIMINUIR a taxa de mutação quando o sistema começasse a estabilizar, pois dessa forma poderiamos fazer o ajuste fino da ponto do braço ate chegar exatamente no ponto 