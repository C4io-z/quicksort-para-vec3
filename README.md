# quicksort-para-vec3
algoritmo para ordenar um array de vetores 3d.

```cpp
class quicksort{
    public:
        quicksort();
        virtual~quicksort();
        std::vector<vec3> elements;
        std::vector<int> indices;
        void startIndex();
        void setIndex();
        int partition (const int start, const int end);
        void swap(const int i, const int j);
        void Quicksort(const int start, const int end);
        void Quicksort();
        void print();
};
```
Exemplo de uso:

```cpp

int main(){
    quicksort obj; ///cria um objeto.
    
    obj.elements = vertices; /// passa um std::vector<vec3> com os vetores que se quer organizar.
    obj.indices = indices;  /// passa um std::vector<int>. estes indices apontavan para um objeto no vetor de vertices, porem, apos eles serem organizados, não estarão mais no mesmo lugar. desse jeito ao passar este array para a função, no final ela fara com que todos os indices aponten para o memso vetor que estavan apontando antes do array ser organizado.
    
    obj.startIndex(); /// atribui ao componente w do vetor, a possição dele no array.
    obj.Quicksort(); /// organiza o vetor;
    obj.setIndex(); /// faz com que os indices apontem para o mesmo vetorque apontavam antes do array ser organizado.
    vertices = obj.elements; /// recebe o novo vetor organizado.
    indices = obj.indices; /// recebe os imdices que aponta para o vetor correto
   
 }

```
