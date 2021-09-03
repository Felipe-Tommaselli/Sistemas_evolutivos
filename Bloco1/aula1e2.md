# Primeiro Bloco de teoria- Sistemas Evolutivos Aplicados a Robotica (SC0713)

* gitlab: https://gitlab.com/simoesusp/disciplinas/-/tree/master/SSC0713-Sistemas-Evolutivos-Aplicados-a-Robotica

## Aula 1:

* gravação: https://drive.google.com/file/d/1z0wHTwafRw7nwQTY3KkOe3I3OxQAmEqq/view

### Procedimento de criação de um algoritmo evolutivo

* 1. Inicializar uma população

* 2. Avaliação (mais adaptado => maior nota (fitness))

* 3. Seleção (maior nota => maior probabilidade de ser selecinado)

* 4. Crossover

* 5. Mutação

* 6. Rearranjo da população

> Exemplo

* 1. Iniciar uma população com 10 individuos, associando cada individuo com um "cromossomo" (conjunto de parametros organizados em um vetor)
    * digmaos que queremos fazer café, para isso nosso vetor de parametros sera
    * Cafe => (Agua, Cafe, Acucar, leite), cada individuo da populacao tera uma certta quantidade de cada elemento:
i0 = (10, 3, 5, 10)
...
i9 = (8, 2, 6, 88)

* 2. Dar uma nota para cada individuo, sem segredo

* 3. O método que o simões mais gosta: Elitismo (melhor cruza com todos)
    * **NUNCA MATAR O MELHOR DE TODOS**

* 4. Cruzar (normalmente é só a media, porem há varios metodos)
(10, 3, 5, 10)
    x
(8, 2, 6, 88)
= (9, 2.5, 6.5, 49)

* 5. Mutacao: Sorteia alguns genes e soma (ou subtrai) uma TAXA DE MUTAÇÃO

* 6. Mata alguns individuos e substitui pelos filhos gerados