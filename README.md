# LINK DO PROJETO NO GITHUB PAGES
https://daviflferreira.github.io/projeto-calculadora/

# Calculadora React

## 1. Visão Geral
Projeto de calculadora web desenvolvido com React, com foco em operações básicas, controle de estado e componentização.

## 2. Funcionalidades
- Entrada de dígitos (`0-9`)
- Operações matemáticas (`+`, `-`, `*`, `/`)
- Cálculo com `=`
- Limpeza total com `AC`
- Suporte a números decimais (`.`)
- Bloqueio de múltiplos pontos decimais no mesmo número
- Tratamento de resultados inválidos (`NaN`/`Infinity`)

## 3. Tecnologias
- React
- JavaScript (ES6+)
- CSS3 (Flexbox + Grid)
- Create React App

## 4. Estrutura do Projeto
- `public/`
  - `index.html`: template HTML base
  - `manifest.json`: metadados PWA
  - `robots.txt`: diretivas para crawlers
- `src/`
  - `index.js`: entrada da aplicação
  - `index.css`: estilos globais
  - `main/Calculator.jsx`: lógica da calculadora
  - `main/Calculator.css`: layout da calculadora
  - `components/Button.jsx`: componente de botão
  - `components/Button.css`: estilos dos botões
  - `components/Display.jsx`: componente de visor
  - `components/Display.css`: estilos do visor

## 5. Arquitetura e Fluxo
1. `index.js` renderiza a aplicação no elemento `#root`.
2. `Calculator.jsx` centraliza estado e regras de negócio.
3. `Button.jsx` dispara eventos de clique e envia `label` para funções do pai.
4. `Display.jsx` exibe o valor atual do estado.
5. CSS organiza layout e aparência visual.

## 6. Estado da Calculadora
- `displayValue`: valor mostrado no visor
- `clearDisplay`: define se o próximo dígito limpa o visor
- `operation`: operação atual selecionada
- `values`: dois operandos da conta
- `current`: índice do operando atual (`0` ou `1`)

## 7. Métodos Principais
- `clearMemory()`: restaura estado inicial.
- `addDigit(n)`: adiciona dígitos/ponto ao display e atualiza operando atual.
- `setOperation(operation)`: define operação ou executa cálculo quando necessário.

## 8. Estilização
- Centralização global com Flexbox (`body`, `.app`)
- Calculadora com CSS Grid (`.calculator`)
- Botões com variações visuais:
  - padrão
  - operação (`.operation`)
  - largura dupla (`.double`)
  - largura tripla (`.triple`)
- Título com animação rainbow (`@keyframes colorRotate`)

## 9. Scripts NPM
```bash
npm start
npm run build
npm test
npm run eject
