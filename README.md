# 🧮 Calculadoras de Porcentagem

Um conjunto completo de 13 calculadoras interativas para diversos cálculos percentuais, com design responsivo e cálculos em tempo real.
<!--
![Preview das Calculadoras](https://raw.githubusercontent.com/souzaseven/Site2/Desafios/icon%20eu.ico)
-->
## ✨ Funcionalidades

- **13 Calculadoras Especializadas**:
  - Cálculo de porcentagem básica
  - Determinação de porcentagem entre valores
  - Cálculo de variação percentual
  - Aumento e desconto percentual
  - Cálculo de valor original após aumento/desconto
  - Múltiplos aumentos/descontos consecutivos
  - Divisão percentual em partes iguais
  - Cálculo de ajuste percentual necessário

- **Recursos Avançados**:
  - Cálculos em tempo real (on input)
  - Formatação automática de resultados
  - Identificação de aumentos/descontos
  - Tratamento de séries de porcentagens

## 🛠️ Tecnologias Utilizadas

- **Frontend**:
  - HTML5 semântico
  - CSS3 com Flexbox e Media Queries
  - JavaScript puro (ES6+)

- **Bibliotecas**:
  - Bootstrap 4 (layout responsivo)
  - Google Analytics (métricas)
  - Google AdSense (monetização)

## 📂 Estrutura de Arquivos
calculadora-porcentagem/ <br> 
├── index.html # Estrutura principal<br>
├── style.css # Estilos personalizados<br>
└── script.js # Lógica das calculadoras<br>
<br>

## 🎨 Design e Interface

- **Tema Azul Moderno**:
  - Cores principais: Azul (#007bff) e Branco
  - Cards com bordas arredondadas
  - Sombras sutis para profundidade

- **Responsividade**:
  - Adapta-se de 1 a 5 colunas conforme tamanho da tela
  - Ajustes tipográficos para mobile
  - Espaçamento otimizado para cada dispositivo

## ⚙️ Como Usar

1. Selecione a calculadora desejada
2. Insira os valores nos campos correspondentes
3. O resultado é calculado automaticamente

**Exemplo de Cálculo Básico**:
```javascript
function calcular1() {
    var porcentagem = parseFloat(document.getElementById('c1v1').value);
    var valor = parseFloat(document.getElementById('c1v2').value);
    if (!isNaN(porcentagem) && !isNaN(valor)) {
        var resultado = (porcentagem / 100) * valor;
        document.getElementById('r1').textContent = ' ' + resultado.toFixed(2);
    }
}
```
 
🌟 Destaques do Código <br>
Cálculo de Múltiplos Aumentos: <br>
```javascript
function calcular7() {
    var valorInicial = parseFloat(document.getElementById('c7v1').value);
    var porcentagens = document.getElementById('c7v2').value.split(',').map(parseFloat);
    if (!isNaN(valorInicial) && porcentagens.every(v => !isNaN(v))) {
        var resultado = porcentagens.reduce((acc, p) => acc * (1 + p / 100), valorInicial);
    }
}
```
Detecção Automática de Aumento/Desconto:
```javascript
if (resultado > 0) {
    texto += ' (aumento)';
} else if (resultado < 0) {
    texto += ' (desconto)';
}
```
📱 Responsividade <br>
O layout se adapta a: <br>

Dispositivo	Colunas	Largura Máxima <br>
Mobile (<576px)	1	100% <br> 
Tablet (≥576px)	2	50% <br>
Laptop (≥768px)	3	33.33% <br>
Desktop (≥992px)	4	25% <br>
Wide (≥1400px)	5	20% <br>





