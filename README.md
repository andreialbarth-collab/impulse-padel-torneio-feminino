# Impulse Padel BVB — Gestor de torneio

Aplicação web estática para organizar torneio de padel com 16 participantes.

## Como executar
- Abra `index.html` no navegador; ou
- Publique os arquivos deste projeto em um projeto Vercel (framework: **Other**, sem comando de build).

## Funcionalidades
- Cadastro de 8 jogadores de direita e 8 de esquerda.
- Geração progressiva de 5 rodadas com 4 jogos por rodada; a rodada seguinte é liberada quando todos os placares da rodada atual estão preenchidos.
- Rodadas 1 e 2: sorteio aleatório das duplas.
- Rodadas 3 a 5: duplas niveladas conforme a classificação individual de cada lado (1º direita + 8º esquerda, 2º + 7º etc.).
- Confrontos embaralhados independentemente do ranking, tentando evitar a repetição exata de confronto em rodadas consecutivas.
- Registro de placares sem vantagem, com empate permitido.
- Classificação individual: vitória 3 pontos, empate 1, derrota 0; desempate por pontos de classificação, saldo de pontos e pontos feitos.
- Exibição de adversários lado a lado em cada jogo.

## Observações
- As rodadas 1 e 2 são sorteadas no início. A rodada 3 é gerada após preencher todos os placares da rodada 2; as rodadas 4 e 5 são geradas da mesma forma, usando a classificação atualizada. Os placares são mantidos apenas enquanto a página está aberta; recarregar a página reinicia o torneio. Faça uma captura ou anote os resultados antes de sair.
- O horário das quadras mostrado nos cartões é ilustrativo e pode ser ajustado conforme a organização. A previsão geral informada é 14h–18h.
- “Evitar repetição” é uma preferência do sorteio: o algoritmo tenta evitar confrontos idênticos à rodada anterior; em situações sem combinação alternativa, pode não conseguir eliminar todas as repetições.
