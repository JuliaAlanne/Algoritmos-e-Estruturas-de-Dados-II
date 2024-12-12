
Discente: Júlia Alanne Silvino dos Santos

Matrícula: 20240001215

## Desempenho de algoritmos

### Objetivo:
Avaliar o desempenho de dois algoritmos fornecidos(solver_closest.ipynb e solver_kth_largest.ipynb) considerando diversas entradas aleatórias e reproduzíveis, variando o tamanho do vetor de entrada até um valor N grande.

### Requisitos
* Instrumentar os códigos fornecidos com o módulo time para medir o tempo de execução.
*  Realizar testes com vetores de tamanhos variados.
*   Para cada tamanho de vetor, realizar múltiplas execuções e calcular o tempo médio e o
intervalo de confiança.
* Gerar gráficos com tamanho do vetor (eixo x), tempo médio de execução (eixo y), e intervalos de confiança como barras de erro no gráfico.

  
```python
import numpy as np
import matplotlib.pyplot as plt
from time import time
from scipy.stats import t

def findClosestValue(tree, target):
    """
    Finds the value in a binary search tree that is closest to the given target value.

    This function begins the search for the closest value from the root of the binary search tree.
    It works by recursively (or sequentially) exploring the tree, narrowing down the search based on the target value
    and the current node's value. The closest value is constantly updated throughout the search process.

    Parameters:
    tree (BinarySearchTree): The binary search tree object in which to find the closest value.
                             It is expected to have a 'root' attribute that points to the root node of the tree.
    target (int or float): The target value for which the closest value in the binary search tree is sought.

    Returns:
    int or float: The value in the binary search tree that is closest to the target value.
    """
    return findClosestValueInBstHelper(tree.root, target, tree.root.value)


def findClosestValueInBstHelper(node, target, closest):
    if node is None:
        return closest
    if abs(target - closest) > abs(target - node.value):
        closest = node.value
    if target < node.value:
        return findClosestValueInBstHelper(node.left_child, target, closest)
    elif target > node.value:
        return findClosestValueInBstHelper(node.right_child, target, closest)
    else:
        return closest


def solver_closest(arr, k):

    return findClosestValue(bst, k)


def findKthLargestValue(tree, k):
    """
    Finds the kth largest integer in a Binary Search Tree (BST).

    The function traverses the BST in an in-order manner to collect the node values in a sorted list.
    It then returns the kth largest value from this list. The BST is assumed to contain only integer values.
    In case of duplicate integers, they are treated as distinct values.
    The kth largest integer is determined in the context of these distinct values.

    Parameters:
    tree (BST): the Binary Search Tree (BST).
    k (int): A positive integer representing the kth position.

    Returns:
    int: The kth largest integer present in the BST.
    """
    sortedNodeValues = []
    inOrderTraverse(tree.root, sortedNodeValues)
    return sortedNodeValues[len(sortedNodeValues) - k]


def inOrderTraverse(node, sortedNodeValues):
    if node is None:
        return

    inOrderTraverse(node.left_child, sortedNodeValues)
    sortedNodeValues.append(node.value)
    inOrderTraverse(node.right_child, sortedNodeValues)


def solver_kth_largest(arr, target):

    return findKthLargestValue(arr, target)




![video]()
