**Árvore AVL em C**

Este é um projeto que implementa uma Árvore AVL em linguagem C. A Árvore AVL é uma árvore binária de busca balanceada, onde a diferença máxima de altura entre os seus subnodos esquerdo e direito é no máximo 1, garantindo assim que a árvore permaneça balanceada.

A estrutura de dados utilizada é a seguinte:

```c
typedef struct nodo {
    int valor;
    struct nodo *esq;
    struct nodo *dir;
    struct nodo *pai;
    int h;
} Nodo;
```

Cada nodo possui um valor inteiro, além de ponteiros para os seus nodos filhos (esquerdo e direito), o nodo pai e a altura do nodo (h).

O projeto inclui as seguintes funções:

- `Nodo* criarNodo(int v)`: Cria e inicializa um novo nodo com o valor v.

- `int fb(Nodo *p)`: Função de balanceamento que calcula o fator de balanceamento de um nodo, que é a diferença entre as alturas do subnodo esquerdo e do subnodo direito.

- `Nodo* rotDir(Nodo *raiz)`: Realiza uma rotação à direita em torno de um nodo raiz, para balancear a árvore.

- `Nodo* rotEsq(Nodo *raiz)`: Realiza uma rotação à esquerda em torno de um nodo raiz, para balancear a árvore.

- `Nodo* rotEsqDir(Nodo *raiz)`: Realiza uma rotação à esquerda seguida de uma rotação à direita, para balancear a árvore.

- `Nodo* rotDirEsq(Nodo *raiz)`: Realiza uma rotação à direita seguida de uma rotação à esquerda, para balancear a árvore.

- `Nodo* balancear(Nodo *raiz)`: Função de balanceamento que verifica se a árvore está desbalanceada em algum nodo e realiza as rotações necessárias para corrigir o balanceamento.

- `void mostraArvore(Nodo *p, int nivel)`: Função recursiva que exibe a árvore de forma indentada, mostrando os valores dos nodos, suas alturas e fatores de balanceamento.

- `Nodo* inserirNodo(Nodo *raiz, int v)`: Insere um novo nodo na árvore AVL, mantendo o balanceamento.

- `Nodo* buscar(Nodo *raiz, int v)`: Busca um valor na árvore AVL e retorna o nodo correspondente.

- `Nodo* excluir(Nodo *raiz, int v)`: Exclui um valor da árvore AVL, mantendo o balanceamento.

O programa principal (`main`) é um loop interativo que permite ao usuário inserir, excluir e buscar valores na árvore AVL. A árvore é exibida após cada operação para visualização.

Sinta-se à vontade para utilizar e modificar este código de acordo com suas necessidades. Para mais informações sobre Árvores AVL e as operações implementadas, consulte os comentários no código.

*Autor: Nícolas Gabriel Meneses de Jesus*
