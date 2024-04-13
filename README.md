# Mergulhando no Universo dos Sets: Um Guia Completo

O set do C++ é como um universo ordenado onde cada elemento é uma estrela única e brilhante. Ele é uma estrutura de dados da STL que garante a individualidade dos elementos, mantendo-os organizados de forma crescente e permitindo acessá-los com eficiência. 🪐

## Explorando as Funcionalidades:

### Criação do Set:

Inclua a biblioteca `<set>`:

```cpp
#include <set>
```

Declare seu set com o tipo de elemento desejado:

```cpp
set<int> meu_set; // Set de inteiros
set<string> conjunto_palavras; // Set de strings
```

### Adicionando Estrelas (Elementos):

Use a função `insert()` para adicionar elementos, evitando repetições:

```cpp
meu_set.insert(5);
meu_set.insert(10);
meu_set.insert(5); // Este 5 será ignorado, pois já existe no set
```

### Removendo Estrelas (Elementos):

Elimine elementos indesejados com a função `erase()`:

```cpp
meu_set.erase(10); // Remove o elemento 10
```

Você também pode remover usando um iterador:

```cpp
set<int>::iterator it = meu_set.find(5);
meu_set.erase(it); // Remove o elemento apontado pelo iterador
```

### Buscando Estrelas (Elementos):

Encontre elementos específicos com a função `find()`, que retorna um iterador:

```cpp
set<int>::iterator it = meu_set.find(5);
if (it != meu_set.end()) {
    // Elemento encontrado!
} else {
    // Elemento não encontrado
}
```

### Outras Funções Estelares:

- `begin()`: Retorna um iterador para o primeiro elemento.
- `end()`: Retorna um iterador para o elemento após o último.
- `empty()`: Verifica se o set está vazio (retorna true se estiver).
- `size()`: Retorna o número de elementos no set.
- `clear()`: Remove todos os elementos do set.
- `lower_bound(x)`: Retorna um iterador para o primeiro elemento que não é menor que x.
- `upper_bound(x)`: Retorna um iterador para o primeiro elemento que é maior que x.

### Percorrendo o Universo (Set):

Use iteradores para navegar pelo set em ordem crescente:

```cpp
for (set<int>::iterator it = meu_set.begin(); it != meu_set.end(); ++it) {
    cout << *it << " ";
}
```

### Exemplo de Aplicação: Frequência na Aula

O desafio "Frequência na Aula" demonstra o poder do set para lidar com elementos únicos. O objetivo é identificar o número real de alunos presentes, mesmo com números de registro repetidos na lista de presença.

```cpp
#include <iostream>
#include <set>

int main() {
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);

    int n;
    cin >> n;

    set<int> lista_presenca;

    while (n--) {
        int numero;
        cin >> numero;
        lista_presenca.insert(numero);
    }

    cout << lista_presenca.size() << endl;

    return 0;
}
```

Ao utilizar o set, garantimos que cada número de registro seja contabilizado apenas uma vez, independentemente de quantas vezes ele tenha sido inserido na lista. A função `size()` nos dá o número exato de alunos presentes, resolvendo o problema de forma elegante e eficiente.

## Conclusão

O set é uma ferramenta poderosa para quem precisa lidar com elementos únicos e ordenados. Com sua interface simples e eficiência, ele se torna um aliado valioso em diversos desafios de programação. �
