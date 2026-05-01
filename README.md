# 💣 Campo Minado em C
 
Implementação do clássico jogo **Campo Minado** no terminal, desenvolvida em C com foco em estruturas de dados, lógica de jogo e validação de entrada.
 
---
 
## 🎮 Como Jogar
 
O objetivo é abrir todas as casas do tabuleiro que **não contêm bombas**. Você perde se abrir uma bomba. Use os números revelados para deduzir onde estão as bombas e marque-as com bandeiras.
 
**Ações disponíveis:**
- `R` — Revelar uma casa
- `F` — Colocar/remover bandeira
**Formato de entrada:** `AÇÃO LINHA COLUNA` (ex: `R 2 C`)
 
---
 
## 🗂️ Estrutura de Dados
 
O tabuleiro é representado por **4 matrizes de inteiros independentes**:
 
| Matriz | Descrição |
| :--- | :--- |
| `campoBombas` | Posição das bombas (1 = bomba, 0 = vazia) |
| `campoAberto` | Casas já reveladas pelo jogador |
| `campoBandeira` | Casas marcadas com bandeira |
| `campoVizinhos` | Quantidade de bombas adjacentes |
 
> **Por que matriz?** Acesso direto por linha/coluna, verificação eficiente de vizinhos e separação clara de responsabilidades entre os estados do jogo.
 
---
 
## ⚙️ Funcionalidades
 
- **Tabuleiro configurável:** Linhas (5-15), colunas (5-15) e número de bombas definidos pelo jogador.
- **Revelação recursiva:** Casas sem bombas vizinhas revelam automaticamente suas adjacentes.
- **Validação de entrada:** Ação, linha e coluna são validados com mensagens de erro claras.
- **Condição de vitória:** Todas as casas sem bomba abertas e todas as bombas marcadas.
---
 
## 🚀 Como Compilar e Executar
 
**Pré-requisito:** GCC instalado.
 
```bash
# Compilar
gcc campominado.c -o campominado
 
# Executar (Linux/Mac)
./campominado
 
# Executar (Windows)
campominado.exe
```
 
---
 
## 👨‍💻 Autor
 
- Christiano Gonçalves Araujo

PUC Minas — Engenharia de Software
