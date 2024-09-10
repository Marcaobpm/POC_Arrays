# POC_Arrays
Neste README, vamos explorar algumas das operações avançadas de JavaScript com arrays, que podem ser utilizados em conjunto com o HTML para manipular e exibir dados dinamicamente. As operações incluem: Array Original, Sort, Map, Reduce, Filter e o Spread Operator.

# Operações com Arrays em JavaScript
1. Array Original
O Array Original é simplesmente um array que armazena uma lista de elementos. Ele pode conter qualquer tipo de dado, como números, strings, objetos, ou até outros arrays.

![image](https://github.com/user-attachments/assets/d394392b-8116-4014-af2a-15111e8b2134)

2. Sort
A função sort() em JavaScript é usada para ordenar os elementos de um array. Por padrão, ele classifica os elementos como strings em ordem alfabética. Para ordenar números, é necessário fornecer uma função de comparação.

![image](https://github.com/user-attachments/assets/daf56067-8425-4d61-bf4c-5e5f6ec24026)

3. Map
O map() é usado para criar um novo array com o resultado de uma função aplicada a cada elemento do array original. Ele não altera o array original, mas retorna um novo array.

![image](https://github.com/user-attachments/assets/a5bed5c0-889a-4083-a0ea-3d72107b9919)

4. Reduce
A função reduce() é usada para reduzir o array a um único valor. Ele aplica uma função "acumuladora" a cada elemento do array, resultando em um valor final.

![image](https://github.com/user-attachments/assets/fb196c99-257b-4d2e-9a66-7673b83e21fa)

5.Filter
A função filter() é utilizada para criar um novo array com todos os elementos que passam em um determinado teste (função de callback). Essa função não altera o array original, mas retorna um novo array contendo apenas os elementos que atenderem ao critério definido.

![image](https://github.com/user-attachments/assets/b3a45727-5662-4a78-b063-021a9581658a)

6.Spread Operator
O Spread Operator (...) é usado para expandir elementos de um array ou objeto iterável em lugares onde múltiplos elementos são esperados (como em uma lista de argumentos de uma função ou para concatenar arrays). Ele é útil para clonar arrays, combinar arrays ou passar argumentos de um array para uma função.

![image](https://github.com/user-attachments/assets/15fa5598-fba2-407b-8afd-0d51049f6645)

[Uploading jav (1).js…]()// Array original
let originalArray = [5, 12, 8, 130, 44];

// Exibe o array original
document.getElementById("original-array").textContent = originalArray.join(", ");

// Função para demonstrar o método sort()
function applySort() {
    let sortedArray = [...originalArray];
    sortedArray.sort((a, b) => a - b);
    document.getElementById("result-sort").textContent = "Array ordenado: " + sortedArray.join(", ");
}

// Função para demonstrar o método map()
function applyMap() {
    let mappedArray = originalArray.map(num => num * 2);
    document.getElementById("result-map").textContent = "Array mapeado: " + mappedArray.join(", ");
}

// Função para demonstrar o método reduce()
function applyReduce() {
    let sum = originalArray.reduce((acc, curr) => acc + curr, 0);
    document.getElementById("result-reduce").textContent = "Soma dos elementos: " + sum;
}

// Função para demonstrar o método filter()
function applyFilter() {
    let filteredArray = originalArray.filter(num => num > 10);
    document.getElementById("result-filter").textContent = "Array filtrado: " + filteredArray.join(", ");
}

// Função para demonstrar o spread operator
function applySpread() {
    let array2 = [7, 21, 34];
    let combinedArray = [...originalArray, ...array2];
    document.getElementById("result-spread").textContent = "Array combinado: " + combinedArray.join(", ");
}

[Uploading stylebody {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    margin: 0;
    padding: 0;
}

.container {
    width: 90%;
    margin: 40px auto;
    background-color: #fff;
    padding: 20px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1 {
    text-align: center;
    color: #333;
}

.array-section {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
}

.method {
    background-color: #e0f7fa;
    padding: 15px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

button {
    background-color: #00796b;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #004d40;
}

p {
    color: #333;
    margin: 10px 0;
}
.css…]()


[Uploading POC_a<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Métodos de Array em JavaScript</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Métodos de Array em JavaScript</h1>
        <div class="array-section">
            <div class="method">
                <h3>Array Original:</h3>
                <p id="original-array"></p>
            </div>

            <div class="method">
                <h3>sort()</h3>
                <p>Ordena o array:</p>
                <button onclick="applySort()">Executar sort()</button>
                <p id="result-sort"></p>
            </div>

            <div class="method">
                <h3>map()</h3>
                <p>Multiplica os elementos por 2:</p>
                <button onclick="applyMap()">Executar map()</button>
                <p id="result-map"></p>
            </div>

            <div class="method">
                <h3>reduce()</h3>
                <p>Soma todos os elementos:</p>
                <button onclick="applyReduce()">Executar reduce()</button>
                <p id="result-reduce"></p>
            </div>

            <div class="method">
                <h3>filter()</h3>
                <p>Filtra números maiores que 10:</p>
                <button onclick="applyFilter()">Executar filter()</button>
                <p id="result-filter"></p>
            </div>

            <div class="method">
                <h3>spread operator</h3>
                <p>Combina dois arrays:</p>
                <button onclick="applySpread()">Executar spread</button>
                <p id="result-spread"></p>
            </div>
        </div>
    </div>

    <script src="jav.js"></script>
</body>
</html>
rray.html…]()






