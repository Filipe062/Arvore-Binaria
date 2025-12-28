strutura de Dados: Árvore Binária de Busca (BST)
Este repositório contém uma implementação robusta de uma Árvore Binária de Busca (Binary Search Tree) em Java, desenvolvida como parte dos estudos de estruturas de dados.

Shutterstock

📌 Sobre o Projeto
A classe ArvoreBinaria<T> utiliza o conceito de Generics, permitindo que a árvore armazene qualquer tipo de dado, desde que ele implemente a interface Comparable (necessária para realizar as comparações de "maior" ou "menor" durante a inserção e busca).

Características principais:
Ordenação: Elementos menores à esquerda, elementos maiores à direita.

Flexibilidade: Suporta qualquer objeto comparável (Integer, String, objetos customizados).

Recursividade: Algoritmos de inserção e exibição otimizados via recursão.

🚀 Funcionalidades
A implementação conta com as seguintes operações:

Inserção (inserir): Adiciona um novo nó na posição correta, mantendo a propriedade da BST.

Exibição In-Order (exebirInOrdem): Percorre a árvore de forma que os elementos sejam exibidos em ordem crescente.

Remoção (remover): Remove um nó específico, tratando os três casos possíveis:

Nó folha (sem filhos).

Nó com apenas um filho.

Nó com dois filhos (reorganizando a árvore através do sucessor/antecessor).

🛠️ Estrutura do Código
O projeto está organizado no pacote one.digitalone e é composto por:

ArvoreBinaria.java: Classe principal com a lógica de manipulação.

BinNo.java: Classe que representa o nó da árvore (contendo o dado e as referências para os nós esquerdo e direito).

💻 Exemplo de Uso
Java

import one.digitalone.ArvoreBinaria;

public class Main {
    public static void main(String[] args) {
        ArvoreBinaria<Integer> minhaArvore = new ArvoreBinaria<>();

        minhaArvore.inserir(13);
        minhaArvore.inserir(10);
        minhaArvore.inserir(25);
        minhaArvore.inserir(2);
        minhaArvore.inserir(12);

        // Exibe: 2, 10, 12, 13, 25
        minhaArvore.exebirInOrdem();

        minhaArvore.remover(10);
        minhaArvore.exebirInOrdem();
    }
}
