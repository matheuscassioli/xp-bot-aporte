# 🤖 XP Bot Aporte

Um bot automatizado desenvolvido para auxiliar no planejamento e na tomada de decisão dos meus aportes recorrentes de investimentos (ações e FIIs) com foco em um ciclo de 15 a 30 dias.

## 🎯 Objetivo
Auxiliar no momento do aporte periódico. O bot avalia os ativos da carteira atual, compara com regras de preço/oportunidade e gera um relatório prático para otimizar as compras na corretora (XP).

## ⚙️ Funcionalidades Planejadas
- **Análise de Ativos:** Varredura para identificar quais ativos estão com preços atrativos para o próximo aporte.
- **Ciclo Otimizado:** Alinhado ao planejamento de 15 a 30 dias.
- **Automação:** Execução automatizada via GitHub Actions.

## 🚀 Como rodar

```bash
npm install
npm run dev   # executa src/index.ts diretamente (via tsx)
```

Cotações via Yahoo Finance (API não-oficial, gratuita, sem token) usando o sufixo `.SA` para tickers da B3.

Edite `src/config/carteira.ts` com os seus tickers e preços teto.

Build de produção:

```bash
npm run build
npm start
```

## 📊 Dashboard

Existe um dashboard web (React) para visualizar o relatório de aporte no navegador, com cards de resumo, gráfico de margem de segurança por ativo e tabela detalhada. Ele consulta uma API local que roda a mesma análise do bot on-demand — inclui um botão "Atualizar" para reconsultar as cotações.

Rode os dois processos (em terminais separados):

```bash
npm run server                          # API em http://localhost:3001
cd web && npm install && npm run dev    # dashboard em http://localhost:5173
```
