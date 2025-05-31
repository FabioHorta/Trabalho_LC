
<<<<<<< HEAD
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
=======
# 🧠 Sistema Pericial para Recomendação de Restaurantes

Este projeto consiste num sistema pericial em **Prolog** que recomenda restaurantes com base em critérios dados pelo utilizador, como localização, preço, tipo de comida, dietas disponíveis, entre outros. A base de conhecimento é construída a partir de um ficheiro `.csv` com dados reais de restaurantes.

---
```
## 📁 Estrutura do Projeto

```plaintext
Trabalho_Pratico/
├── base_conhecimento.pl   # Fatos extraídos do CSV
├── perito.pl              # Sistema pericial (motor de inferência)
├── test.pl                # Base de conhecimento com regras e objetivo
├── restaurantes.csv       # Ficheiro original com dados dos restaurantes
├── exportador.py          # Script Python para gerar o base_conhecimento.pl
└── README.md              # Este ficheiro


```
---

## ⚙️ Tecnologias Usadas

- **Prolog** (SWI-Prolog)
- **Git / GitHub**
- **Git LFS** (para ficheiros grandes como `restaurants.pl`)

---

## 🚀 Como Correr o Sistema
 swipl perito.pl
 
### 1. Gera a base de conhecimento

```

?- consult(perito).
?- perito.

Segue as instruções interativas:

Consulta a base de conhecimento: test.

Responde às perguntas com base nas tuas preferências

O sistema recomendará um restaurante
```

📌 Funcionalidades
```
✅ Perguntas adaptativas: só pergunta atributos relevantes

✅ Validação automática de inputs (cidades, tipos de comida, etc.)

✅ Sistema extensível a outras áreas (basta trocar o objectivo/1 e os atributos)

✅ Suporte a grandes volumes de dados (via Git LFS)

✅ Suporte a múltiplas dietas, prémios, e estilos de cozinha
```

```
restaurante('farol_da_esperanca', 'belmonte', 1, 4.0, ['portuguese', 'european'], ['vegetariano'], [], 'sim').
localizacao('farol_da_esperanca', 39.676, -7.338).
```
🙋‍♂️ Autores
```
Fábio Horta
Beatriz Patrício
```
>>>>>>> 5c8198aea253f7b7cfd0453c0a19bc52fdb47341
