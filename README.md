# Q‑Learning Labirinto — Aprendizado por Reforço Interativo

Este repositório contém uma aplicação web interativa que demonstra o funcionamento do **Q‑Learning**, um algoritmo fundamental de Aprendizado por Reforço (Reinforcement Learning). O grande diferencial deste projeto é que todo o processamento matemático, o treinamento do agente e a atualização da tabela Q são executados **nativamente no navegador do usuário**, via WebAssembly (Pyodide), sem necessidade de qualquer servidor backend ou instalação local.

## Aplicação ao Vivo

Você pode testar a aplicação diretamente pelo link abaixo:

**[Acessar o Projeto (GitHub Pages)](https://samuel-sanches-br.github.io/q-learning-labirinto/)**

## Sobre o Projeto

A aplicação permite que o usuário:

- Ajuste os hiperparâmetros do Q‑Learning (α, γ, ε) e as recompensas (penalidade por passo, recompensa do tesouro).
- Treine o agente por 1 episódio (com visualização) ou em lote de 100 episódios.
- **Edite o labirinto** dinamicamente: adicione/remova paredes, reposicione o tesouro.
- Utilize o **Modo Manual**: controle o agente passo a passo e veja, em tempo real, a equação de Bellman sendo aplicada com os valores numéricos – ideal para entender a mecânica de atualização do Q‑value.
- Visualize os Q‑values do estado atual através de barras horizontais intuitivas.

## Funcionalidades Principais

- **Execução Client‑Side:** 100% no navegador, sem servidor, usando Pyodide.
- **Hiperparâmetros ajustáveis:** α (taxa de aprendizado), γ (fator de desconto), ε (exploração).
- **Recompensas configuráveis:** penalidade por passo e valor do tesouro.
- **Editor de labirinto:**
  - Clique para adicionar/remover paredes.
  - Defina a posição do tesouro com um clique.
  - Botões para labirinto aleatório, limpar paredes e resetar o padrão.
- **Treinamento flexível:**
  - Um episódio com animação.
  - Lote de 100 episódios para convergência mais rápida.
  - Reset da tabela Q a qualquer momento.
- **Modo Manual:**
  - Controle o agente seta por seta.
  - A cada movimento, a aplicação exibe:
    - Recompensa imediata (r).
    - Cálculo do TD target e TD erro.
    - Atualização do Q‑value (equação de Bellman).
    - Comparação entre Q antigo e novo.


## Conceitos Demonstrados

| Conceito | O que o projeto mostra |
|----------|------------------------|
| **Q‑Learning** | Atualização da tabela Q usando a equação de Bellman. |
| **Exploração vs. Explotação** | Parâmetro ε controla a taxa de ações aleatórias. |
| **Recompensa imediata (r)** | Penalidade por passo e recompensa do objetivo. |
| **TD target e TD erro** | Cálculo exibido no modo manual. |
| **Desconto futuro (γ)** | Influência das recompensas futuras nas decisões. |
