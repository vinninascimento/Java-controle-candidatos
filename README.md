# Controle de Candidatos - Processo Seletivo

Este repositório contém um exemplo de código em Java que demonstra um sistema de controle de candidatos para um processo seletivo. O sistema toma decisões com base no salário pretendido pelos candidatos em relação ao valor base salarial. Ele também simula a seleção de candidatos para entrevista e o contato com eles.

## Case 1: Seleção de Candidatos

Vamos imaginar um processo seletivo com um valor base salarial de R$ 2.000,00 e o salário pretendido pelo candidato. O sistema toma decisões da seguinte forma:

```
if (valorSalarioBase > valorSalarioPretendido) {
    System.out.println("LIGAR PARA O CANDIDATO");
} else if (valorSalarioBase == valorSalarioPretendido) {
    System.out.println("LIGAR PARA O CANDIDATO, COM CONTRA PROPOSTA");
} else {
    System.out.println("AGUARDANDO RESULTADO DOS DEMAIS CANDIDATOS");
}
```
## Case 2: Seleção de Candidatos para Entrevista
No segundo caso, o sistema garante que, diante das inúmeras candidaturas, sejam selecionados apenas no máximo 5 candidatos para entrevista, desde que o salário pretendido seja menor ou igual ao salário base.

```
// Array com a lista de candidatos
String[] candidatos = {"FELIPE", "MÁRCIA", "JULIA", "PAULO", "AUGUSTO", "MÔNICA", "FABRÍCIO", "MIRELA", "DANIELA", "JORGE"};

// Método que simula o valor pretendido
static double valorPretendido() {
    return ThreadLocalRandom.current().nextDouble(1800, 2200);
}
```
## Case 3: Listagem de Candidatos Selecionados
No terceiro caso, é o momento de imprimir a lista dos candidatos selecionados para disponibilizar ao RH para entrar em contato.

## Case 4: Contato com Candidatos
No quarto caso, o RH realiza uma ligação com no máximo 03 tentativas para cada candidato selecionado. O sistema registra as tentativas e exibe mensagens de acordo com o resultado.

```
if (contatoBemSucedido) {
    System.out.println("CONSEGUIMOS CONTATO COM " + candidato + " APÓS " + tentativas + " TENTATIVA(S)");
} else {
    System.println("NÃO CONSEGUIMOS CONTATO COM O " + candidato);
}

```
