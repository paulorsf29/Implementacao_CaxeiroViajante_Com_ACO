# Implementação de IA Evolutiva: ACO para o Problema do Caixeiro Viajante (TSP)

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![AI](https://img.shields.io/badge/AI-Evolutionary-orange.svg)
![ACO](https://img.shields.io/badge/Algorithm-Ant%20Colony%20Optimization-red.svg)
![TSP](https://img.shields.io/badge/Problem-TSP-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)
![License](https://img.shields.io/badge/License-MIT-purple.svg)

Este projeto apresenta uma implementação do **Algoritmo de Otimização por Colônia de Formigas (ACO)** aprimorado com **refinamento 2-Opt** para resolver o clássico **Problema do Caixeiro Viajante (TSP)**, utilizando **dados reais de 48 cidades do Rio Grande do Norte – Brasil**.

O objetivo é encontrar a menor rota possível que passe por todas as cidades exatamente uma vez e retorne ao ponto de origem, utilizando técnicas de **Inteligência Artificial Evolutiva**.

## 📊 Resultados Obtidos

| Cidades | Distância (km) | Tempo (s) | Comparação com GLPK |
|--------|------------------|----------|----------------------|
| 6      | 344.6            | 0.81     | -0.09%              |
| 7      | 487.9            | 1.43     | +11.32%             |
| 12     | 778.4            | 4.92     | +15.71%             |
| 24     | 1328.8           | 38.14    | -0.83%              |
| 36     | 1586.8           | 128.05   | **-7.70%**          |
| 48     | 1939.0           | 338.38   | -0.17%              |

✅ Melhor desempenho encontrado com **36 cidades**, superando o GLPK em **-7,70%**  
✅ O método **ACO + 2-Opt** mostrou excelente eficiência em instâncias maiores  

Resultado detalhado

<img width="566" height="155" alt="image" src="https://github.com/user-attachments/assets/db52139c-5b17-48b3-ac22-645ef197ac47" /> 

## 🔧 Funcionalidades do Projeto

- Implementação completa do ACO com parâmetros ajustáveis:  
  - `α` – influência do feromônio  
  - `β` – influência heurística  
  - `ρ` – taxa de evaporação  
  - `Q` – quantidade de feromônio

- Refinamento **2-Opt aplicado automaticamente** em instâncias maiores que 20 cidades  
- Fixação do ponto inicial em **Angicos – RN**  
- Dashboard com **6 gráficos analíticos comparativos**  
- Mapas geográficos das rotas otimizadas  
- Comparação com:
  - Solução usando **GLPK**
  - Dados de artigo científico de referência
- Cálculo das distâncias considerando **fator de tortuosidade = 1.29**

## 🗂 Estrutura do Projeto
 IMPLEMENTAÇÃO_DE_IA_EVOLUTIVA.ipynb

- 📍 Dados reais das 48 cidades do RN (coordenadas) -
- 🧮 Cálculo de distâncias geográficas -
- 🐜 Implementação do ACO
- 🔁 Refinamento com 2-Opt
- 📊 Visualizações gráficas
- 🗺 Mapas das rotas otimizadas
- 📋 Tabelas comparativas detalhadas

## 🚀 Como Executar o Projeto

1. Instale as bibliotecas necessárias no terminal:
```bash
pip install pandas
pip install matplotlib
pip install networkx
```
2. Abra o Arquivo
   IMPLEMENTAÇÃO_DE_IA_EVOLUTIVA.ipynb
3. Execute todas as celulas para rodar o projeto

## 📈 Principais Insights do projeto

- A combinação ACO + 2-Opt apresentou resultados superiores em instâncias maiores

- O desempenho melhora conforme o número de cidades aumenta

- A complexidade do algoritmo cresce em O(n²)

- O algoritmo mostrou-se robusto, eficiente e estável

- Boa adaptação para problemas reais de logística e roteamento

## 🎨 Visualizações Grafica Geradas

- Dashboard com 6 gráficos comparativos

- Mapas geográficos das rotas

- Sequência textual das rotas

- Análise de eficiência em porcentagem

## 👥 Autores

- Davi Tuma

- Paulo Ricardo

- Diogo Siqueira

- Elias Bariani

## 📚 Base Teórica e Referência Principal

Este projeto foi desenvolvido com base no seguinte trabalho acadêmico:

> **Aplicação da meta-heurística de Colônia de Formigas no Problema do Caixeiro Viajante em uma empresa distribuidora de laticínios localizada em Angicos/RN.**  
> **Autores:** Abdiel Jônatas Alves da Silva; Matheus da Silva Menezes  
> Trabalho de Conclusão de Curso – Bacharelado em Ciência e Tecnologia  
> Universidade Federal Rural do Semi-Árido – UFERSA, 2022  
> Disponível em:  
> https://repositorio.ufersa.edu.br/server/api/core/bitstreams/177d84ed-5727-4ece-b374-013af337877b/content

