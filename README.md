# 🍽️ Sistema Pericial de Restaurantes

Sistema desenvolvido em **Prolog** que permite ao utilizador procurar restaurantes com base em diversos critérios personalizados, incluindo localização, tipo de cozinha, orçamento, opções dietéticas e mais.

---

## 🎯 Objetivo

Permitir a **pesquisa inteligente de restaurantes** com base em diferentes critérios definidos pelo utilizador, retornando o restaurante mais próximo que satisfaz as condições impostas.

---

## 🔍 Funcionalidades

O sistema permite filtrar restaurantes pelos seguintes parâmetros:

- 🌍 **País**
- 🏙️ **Cidade**
- 🍝 **Tipo de cozinha** (ex: portuguese, italian)
- 💸 **Preço máximo** (1 = muito barato, 4 = muito caro)
- 🚚 **Entrega** (`sim`, `nao`, `qualquer`)
- 📦 **Takeaway** (`sim`, `nao`, `qualquer`)
- 🌞 **Esplanada** (`sim`, `nao`, `qualquer`)
- 🥗 **Dieta** (`vegano`, `vegetariano`, `sem_gluten`, `nenhuma`)
- 🍳 **Refeição** (`breakfast`, `lunch`, `dinner`)
- 📆 **Dia aberto** (dia da semana ou `"todos"`)
- ⭐ **Avaliação mínima** (ex: `4.0`)
- 🏅 **Prémios** (`sim`, `nao`)
- 📍 **Localização do utilizador** (latitude e longitude)

O sistema calcula a **distância entre o utilizador e o restaurante** para recomendar o mais próximo que cumpra os critérios definidos.

---

## 🧱 Estrutura do Projeto

- `perito.pl`: Contém a lógica do sistema pericial e interface de interação com o utilizador.
- `restaurantes.pl`: Base de conhecimento com os dados dos restaurantes.

### 📦 Exemplo de entrada na base de conhecimento:

```prolog
restaurante('manjar_dos_deuses', 'portugal', 'belmonte', ['european', 'portuguese'], ['lunch', 'dinner'], [], 5, 3.5, [], 'nao', 'nao', 'nao', [], 0.0, 0.0).
```

---

## 💻 Instalação e Execução

### 1️⃣ Instalar o SWI-Prolog

Baixe e instale a partir do site oficial: [https://www.swi-prolog.org/](https://www.swi-prolog.org/)

Para VSCode: Instale a extensão para suporte a arquivos `.pl`.

---

### 2️⃣ Preparar o Projeto

Coloque os arquivos `perito.pl` e `restaurantes.pl` no mesmo diretório.

---

### 3️⃣ Executar o Sistema

#### Com SWI-Prolog:
```prolog
?- consult('perito.pl').
?- perito.
```

#### Ou via terminal (VSCode):
```bash
swipl perito.pl
```

---

## ⚙️ Como Usar

### Menu inicial:
```
Sistema Pericial de Restaurantes
Versão 2025

Comandos disponíveis:
1 - Carregar Base de Conhecimento
2 - Procurar Restaurante
3 - Sair
```

### 📁 Carregar Base de Conhecimento
```
> 1.
Nome do arquivo da Base de Conhecimento (ex: base_conhecimento.pl):
|: restaurantes.
```

### 🔎 Procurar Restaurante
Exemplo de entrada:
```
> 2.
Qual o país? |: portugal
Qual a cidade? |: belmonte
Tipo de cozinha? |: portuguese
Preço máximo (1-4)? |: 5
Quer entrega? (sim/nao/qualquer) |: nao
Quer takeaway? (sim/nao/qualquer) |: nao
Quer esplanada? (sim/nao/qualquer) |: nao
Dieta (vegano, vegetariano, sem_gluten, nenhuma)? |: nenhuma
Refeição? |: dinner
Dia? (mon, tue... ou todos) |: todos
Avaliação mínima? |: 3.5
Restaurantes com prémios? (sim/nao) |: nao
Latitude? |: 2
Longitude? |: 2
```

### ✅ Resultado Esperado
```
Distância aproximada (graus): 2.83
Restaurante recomendado: manjar_dos_deuses
```

---

## 👥 Autores

- **Fábio Horta**
- **Beatriz Patrício**

Este projeto foi desenvolvido como parte de um exercício universitário da cadeira de Lógica Computacional em Prolog, focando na aplicação de **sistemas periciais** para resolver problemas do mundo real.

---

## 📄 Licença

Este projeto é apenas para fins educacionais. Sinta-se à vontade para estudar, modificar e expandir. 🚀

---
