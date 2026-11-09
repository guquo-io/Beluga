# Beluga

Web app de controle de gastos pessoais com rede de apoio: mostra quanto cada pessoa da família contribuiu no mês e para onde o dinheiro foi.

**Status:** em uso real desde 2026.

🎬 Trailer: https://www.youtube.com/watch?v=4w_FWZ0Y9Wc

> Este repositório apresenta o projeto. O código não é público e está disponível sob pedido.

## Contexto

O Beluga começou como uma forma de organizar gastos pessoais e mostrar a quem ajuda com as despesas onde cada contribuição foi usada. Foi o primeiro app que desenvolvi com IA. Algumas funcionalidades (média de gasto diário, limite mensal e importação de extrato) vieram de pedidos de quem usa.

## Funcionalidades

- Perfil para cada pessoa que ajuda, com a marcação de cada gasto: Pix dela, pagamento direto ou gasto dividido.
- Resumo mensal de quanto cada pessoa contribuiu e para onde o dinheiro foi.
- Análise por categoria, com gráfico e filtro de período.
- Limite mensal, também visto por dia, e média de gasto diário.
- Relatório em PDF para mostrar a cada pessoa quanto ela ajudou.
- Importação de extrato bancário (detalhes abaixo).
- Backup e restauração dos dados em arquivo.

## Importação de extrato

- Aceita PDF, OFX e CSV, no formato em que o banco exporta.
- Encontra data, descrição e valor mesmo quando cada banco escreve de um jeito.
- Limpa o nome do lançamento: tira códigos, CPF/CNPJ e prefixos como "Compra no débito".
- Sugere a categoria e lembra como o usuário chamou aquele lugar da última vez.
- Avisa quando um lançamento parece já estar registrado, para não duplicar.
- O usuário confirma item por item antes de entrar no app.

## Decisões

- **Regras próprias em vez de IA na leitura do extrato.** A primeira versão lia o extrato com IA, mas não funcionava bem. A leitura passou a ser feita por regras próprias que rodam no aparelho: o extrato não sai dali, e o mesmo arquivo dá sempre o mesmo resultado.
- **Dados no próprio aparelho.** Por ser dado financeiro, e enquanto ainda estou aprendendo backend e autenticação, os dados ficam salvos no aparelho de quem usa, com backup para baixar e restaurar.

## Tecnologias

- HTML, CSS e JavaScript, num arquivo só.
- Funciona no navegador do celular e pode ser adicionado à tela inicial.
- Chart.js para os gráficos e PDF.js para ler extratos em PDF.
- Dados guardados no navegador do usuário (sem servidor).
- Desenvolvido com ajuda do Claude (vibe coding).

## Código

O código não é aberto. Para ver o código ou conversar sobre o projeto, entre em contato pelo [portfólio](https://guquo-io.github.io).

---

Gustavo Zuqueto · [Portfólio](https://guquo-io.github.io)
