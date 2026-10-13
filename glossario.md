# Glossário

Termos usados no enunciado do estudo de caso ([README.md](README.md)).

| Termo | Significado |
| --- | --- |
| Valor base | Valor “cheio” do jogador, calculado pela API uma única vez, no cadastro, a partir do overall e do potencial, com bônus para jovem promessa (RN06). Não muda depois. |
| Jovem promessa | Jogador com até 21 anos. Pela idade atual, tem +10% no valor de mercado (RN04); se tinha até 21 anos no cadastro, a parte do overall do valor base é multiplicada por (100 + potencial − overall) ÷ 100 (RN06). |
| Valor de mercado | Preço do jogador agora: o valor base ajustado pelos percentuais de condição física, agilidade e idade. É calculado a cada consulta e nunca gravado no jogador; as transações guardam o valor do momento (RN05 e RN17). |
| Condição física | `APTO`, `MAL_CONDICIONADO` ou `DOENTE`. |
| Agilidade | Característica do jogador que altera o desconto de quem não está APTO (RN03). |
| Elenco | Jogadores que pertencem a um clube, com limite de tamanho (RN14). |
| Jogador livre | Jogador sem clube (`club_id` nulo). Só jogador livre pode ser comprado e excluído (RN09 e RN12). |
| Taxa de compra | Valor cobrado na compra, além do valor de mercado (RN13). |
| Custo total | Valor de mercado + taxa de compra; não pode passar de 50% do caixa do clube antes da compra (RN13). |
| Contrato de fidelidade | Criado na compra. Tem uma data de fim; vender antes dela gera multa. |
| Status do contrato | `ATIVO` enquanto o jogador está no clube; na venda, passa a `RESCINDIDO`, se houve multa, ou a `ENCERRADO`, se a fidelidade foi cumprida (RN15). |
| Dias restantes | Dias que faltam até o fim da fidelidade, contados no momento da venda ou da consulta do clube (RN11 e RN15). |
| Valor de compra | O valor de mercado pago pelo clube na compra (sem a taxa). |
| Lucro | Valor de mercado na venda − valor de compra. Pode ser negativo (prejuízo). |
| Comissão de venda | Comissão progressiva sobre o lucro da venda, cobrada só quando há lucro (RN16). |
| Multa por fidelidade | 0%, 5%, 10% ou 20% do valor de mercado na venda, conforme os dias restantes, com teto de 10,00 (RN15). |
| Crédito no caixa | Valor de mercado − multa − comissão, somado ao caixa na venda (RN16). |
| Exclusão lógica | O jogador é marcado como excluído (coluna `excluido_em` no banco) e deixa de aparecer nas consultas e na listagem de jogadores, mas continua no banco, no histórico de transações e nas partidas já jogadas (RN09). |
| Caixa | Verba de transferências do clube (`cash`): começa em 300,00 e só muda por compra e venda. Receitas como bilheteria, patrocínio e premiação ficam fora do sistema. |
| Valor do elenco | Soma dos valores de mercado dos jogadores do clube, calculada a cada consulta (`squad_value`). |
| Patrimônio | Caixa + valor do elenco (`net_worth`). |
| Transação (do histórico) | Registro de uma compra ou venda no histórico do clube (tabela `transacoes`). |
| Variação do caixa | Quanto o caixa mudou numa transação (`cash_change`): negativa na compra e positiva na venda (RN17). |
| Operação atômica | Conjunto de gravações feitas dentro de **uma transação do banco de dados**: ou tudo é gravado, ou nada. Compra, venda, partida e escalação são operações atômicas, assim como a alteração de condição que tira um titular da escalação. Não confundir com a transação do histórico. |
| Paginação | Divisão da listagem de jogadores em páginas (`page`, `limit`), com os metadados em `meta`. |
| Resumo do histórico | Totais calculados pela API (`summary`) sobre as transações filtradas. |
| Teto e piso | Valor máximo e mínimo que um cálculo pode atingir; se o cálculo passar do limite, usa-se o limite (RN05, RN06 e RN15). |
| Indicadores | São oito: os seis atributos (velocidade, `pace`; finalização, `shooting`; passe, `passing`; drible, `dribbling`; defesa, `defending`; físico, `physical`) e o potencial (`potential`), informados no cadastro, mais o `overall`, calculado pela API (RN06). |
| Overall | Nível geral do jogador, **calculado** pela API a partir dos seis atributos, com pesos que dependem da posição (RN06). Nunca é gravado. |
| Potencial | Nível que o jogador pode atingir. Nunca é menor que o maior dos seis atributos (RN06). |
| Escalação | Os titulares de um clube, escolhidos entre os jogadores do elenco. Completa, tem 5: 1 goleiro (GOL) e 4 jogadores de linha, distribuídos numa formação; fica incompleta quando um titular é vendido ou passa a DOENTE, e o clube não joga até escalar de novo (RN19 e RN20). |
| Jogador de linha | Titular que não é o goleiro. A escalação tem 4 (RN19). Na partida, são numerados pela ordem do elenco, do 1º (o mais recuado) ao 4º (o mais avançado): atacam o 4º, o 3º e o 2º, e defendem o goleiro, o 1º e o 2º (RN20). |
| Formação | Distribuição dos 4 jogadores de linha por setor, de trás para frente: defesa (ZAG ou LAT), meio (MEI) e ataque (ATA); o goleiro fica fora da conta. São aceitas `3-1`, `2-2`, `2-1-1` e `1-2-1`, formações usadas no futsal e no futebol de 5 (RN19). |
| Ordem das posições | GOL, ZAG, LAT, MEI e ATA, de trás para frente. Ordena o elenco, a listagem por posição e a escalação, e decide quem ataca e quem defende nos duelos (RN07, RN11, RN19 e RN20). |
| Titular | Jogador escalado; só os titulares entram nos duelos da partida (RN19 e RN20). |
| Partida | Jogo entre dois clubes com escalação completa. O placar é calculado pela API a partir dos atributos dos titulares, sem sorteio (RN20). |
| Mandante e visitante | Os dois clubes da partida; o mandante faz os 3 primeiros ataques, sem outra vantagem: os 6 duelos são sempre disputados (RN20). |
| Duelo | O atributo de ataque de um jogador de linha, que depende da posição dele (finalização para ATA, passe para MEI e drible para ZAG ou LAT), contra a defesa de um titular adversário; vira gol quando o ataque é maior. Titular mal condicionado joga com 15% a menos em cada atributo (RN20). |
| Histórico de partidas | Partidas jogadas, com o placar, as formações e os 6 duelos gravados com os valores do momento (RN21; tabelas `partidas` e `duelos_partida`). |
| Classificação | Tabela com todos os clubes, com pontos (vitória 3, empate 1), jogos, gols e saldo, calculada a cada consulta (RN21). |
| Saldo de gols | Gols marcados menos gols sofridos; é o primeiro desempate da classificação (RN21). |
