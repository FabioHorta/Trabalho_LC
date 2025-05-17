
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
