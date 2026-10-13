# Ficha de avaliação: exemplo preenchido

Estudo de Caso da vaga SENAI/PE – CÓD. 237 DESENVOLVEDOR I (FULLSTACK).

Este documento mostra como fica a ficha de avaliação de um candidato ao fim de todo o processo descrito no [barema](barema.md). O candidato, o repositório, os dados, os horários e as evidências são **fictícios**. Os resultados esperados foram calculados pelas regras do [enunciado](README.md), mas não vêm do roteiro real, que é sigiloso. Nomes de arquivos e hashes são ilustrativos. Para não sugerir uma estrutura de código, esta ficha descreve o que foi avaliado sem citar os arquivos do candidato; na ficha real, cada justificativa aponta os arquivos, os trechos ou as telas avaliados (barema, seção 3.5).

## Como ler esta ficha

- **Roteiros (B1 e F1):** cada item vale a pontuação integral ou zero, e só pontua se **todas** as verificações dele passarem.
- **Critérios de leitura (B2 a B4 e F2 a F4):** três níveis: atende (pontuação integral), atende em parte (metade) e não atende (zero), atribuídos por um avaliador.
- **Diferenciais (B5 e F5):** cada diferencial vale a pontuação cheia ou zero.
- **Esperado e obtido:** em toda verificação que falhou, a ficha mostra o pedido ou o passo, o resultado esperado, o obtido, a regra e a evidência.

## 1. Identificação

| Campo | Registro |
| --- | --- |
| Código do candidato | C-07 (atribuído pelo RH) |
| Nome | preenchido pelo RH depois de fechadas todas as notas |
| Repositório | `https://github.com/exemplo-ficticio/mercado-jogadores` |
| Commit corrigido | `1b2ab32aeb652c21167843eb35c4f6d70e1c2c9f` (branch `main`) |
| Stack | Backend: Node.js 22, TypeScript, NestJS 11, Prisma 6 e PostgreSQL 16. Frontend: React 19 com Vite (template `react-ts`), executado com Node.js 22 |
| Versão dos roteiros | tag `roteiros-v1.0`, commit `a67ff287b71c61283a14542e8f506266caf223c6` |
| Avaliador | Avaliador 1, em todos os critérios |
| Ordem de correção | 7º projeto, pela ordem de recebimento do e-mail de entrega |
| Ambiente | máquina virtual Ubuntu 24.04 LTS (amd64), 4 vCPUs, 8 GB de memória, Docker Engine com Docker Compose v2 e Google Chrome estável; versões exatas na ata |

## 2. Resumo da nota

| Parte | Critério | Máximo | Obtido |
| --- | --- | --- | --- |
| Backend | B1. Roteiro da API | 30 | 25 |
| Backend | B2. Qualidade do código | 10 | 7 |
| Backend | B3. Banco de dados | 6 | 5 |
| Backend | B4. README e histórico do Git | 2 | 1,5 |
| Backend | B5. Diferenciais técnicos | 2 | 2 |
| **Backend** | | **50** | **40,5** |
| Frontend | F1. Roteiro da interface | 30 | 25 |
| Frontend | F2. Qualidade do código | 10 | 7 |
| Frontend | F3. Usabilidade e feedback | 6 | 4 |
| Frontend | F4. README e histórico do Git | 2 | 1 |
| Frontend | F5. Diferenciais de interface | 2 | 2 |
| **Frontend** | | **50** | **39** |
| **Total** | | **100** | **79,5** |

- **Nota final:** 79,5 ÷ 10 = **7,95**.
- **Situação:** **aprovado**. A nota final é de pelo menos 7,0, e as duas partes passam do mínimo de 25 pontos (2,5): 40,5 no backend e 39 no frontend.
- **Entrevista:** 4ª posição na classificação (posição fictícia). Convocado, porque são convocados os 10 primeiros colocados entre os aprovados e todos os empatados na 10ª posição.

## 3. Linha do tempo

| Etapa | Data e hora (horário de Brasília) |
| --- | --- |
| Envio do enunciado | 23/11/2026 (segunda-feira), 9h |
| Fim do prazo de entrega (10º dia após o envio) | 03/12/2026 (quinta-feira), 20h |
| E-mail de entrega do C-07 | 03/12/2026, 19h47min12s |
| Registro dos branches e cópia espelho | 04/12/2026 (sexta-feira), a partir das 12h |
| Preparação, roteiros, sessão de usabilidade e diferenciais | 09/12/2026 (quarta-feira), das 9h05 às 13h05 |
| Leitura do código | 10/12/2026 e 11/12/2026 |
| Consolidação e conferência das notas | 15/12/2026 |
| Resultado e envio desta ficha | 18/12/2026 |

## 4. Entrega e eliminação

### 4.1 Versão corrigida e cópia

- O e-mail de entrega chegou em 03/12/2026, às 19h47min12s, do endereço em que o candidato recebe as comunicações do RH, com cópia para o RH. Ele trazia o nome completo, o link do repositório e o hash completo, de 40 caracteres. Foi o único e-mail de entrega do candidato.
- Em 04/12/2026, às 12h00min07s, a banca registrou os branches e tags de todos os repositórios ao mesmo tempo (`git ls-remote`). No C-07, o branch `main` apontava para o commit informado, e não havia tags.
- A cópia espelho (`git clone --mirror`) foi feita às 12h03 e compactada em `C07-repositorio.tar.gz`, com SHA-256 `4ad82b22dfbdb5fd63e24c2369438bbda18fedc18de08efe0bc497a371163cdc`, registrado em ata.
- Junto com a cópia, foi salvo o histórico de envios (`C07-envios.json`).
- Não houve envio (push) entre o fim do prazo e a cópia.

### 4.2 Situações de eliminação (barema, seção 2)

| # | Situação | Verificação | Resultado |
| --- | --- | --- | --- |
| 1 | E-mail de entrega depois do prazo | recebido em 03/12/2026, às 19h47, antes das 20h (lista de entregas do RH) | não ocorreu |
| 2 | Repositório inacessível sem login | `git ls-remote` e `git clone --mirror` sem credenciais, na primeira tentativa | não ocorreu |
| 3 | Hash ausente ou inalcançável | hash completo, alcançável a partir do branch `main` (`git merge-base --is-ancestor`) | não ocorreu |
| 4 | Commit sem `frontend/` e `backend/` na raiz | as duas pastas estão na raiz do commit | não ocorreu |
| 5 | Tecnologia fora da stack obrigatória | NestJS com TypeScript e Node.js 22; React com Vite; PostgreSQL em contêiner | não ocorreu |
| 6 | Cópia de outro candidato | maior similaridade com outro projeto: 14%, abaixo do limite registrado em ata; nenhum par analisado | não ocorreu |

O projeto segue para a correção completa.

## 5. Preparação do ambiente (barema, seção 3.2)

- **Runtimes instalados pela banca:** Node.js 22 com npm, conforme o item 1 do README do candidato (versão exata na ata). O Docker já faz parte da imagem da máquina virtual.
- **Comandos executados:** copiados literalmente do README da raiz e dos READMEs de `backend/` e `frontend/`, na ordem indicada.

| # | Início | Comando | Resultado |
| --- | --- | --- | --- |
| 1 | 09:05:12 | `cd backend` | ok |
| 2 | 09:05:15 | `cp .env.example .env` | ok (única ação além dos comandos permitida pelo barema) |
| 3 | 09:05:20 | `docker compose up -d db` | imagem pública `postgres:16-alpine` baixada; banco pronto às 09:06:02 |
| 4 | 09:06:10 | `npm ci` | dependências instaladas em 1 min 48 s, pelo `package-lock.json` |
| 5 | 09:08:05 | `npx prisma migrate deploy` | 3 migrations aplicadas |
| 6 | 09:08:20 | `npm run build` | ok |
| 7 | 09:09:02 | `npm run start:prod` | continua em execução; a origem `http://localhost:3000` respondeu às 09:09:20 |
| 8 | 09:09:30 | `cd frontend` (em outro terminal, a partir da raiz) | ok |
| 9 | 09:09:33 | `npm ci` | dependências instaladas em 1 min 05 s |
| 10 | 09:10:45 | `npm run dev` | continua em execução; `http://localhost:5173` abriu no Chrome às 09:11:05 |

- **Comando não executado:** `npm run seed`, marcado no README como opcional (carga de dados de exemplo).
- **Tempo:** 6 min 08 s, contados do primeiro comando, dentro do limite de 30 minutos. Nenhum comando precisou ser repetido.
- **Origem da API e URL do frontend:** as informadas no README, `http://localhost:3000` e `http://localhost:5173`. O script usou `http://localhost:3000/api/v1`.
- **Instantâneo:** tirado às 09:11:20, com o banco recém-criado, e guardado até a divulgação do resultado do estudo de caso.
- **Recriação do banco:** pelo comando do README, `npx prisma migrate reset --force`, às 09:40:02 (antes do B1) e às 10:31:00 (antes do F1), sem erro. A API continuou respondendo.

## 6. Backend

### B1. Roteiro da API: 25 de 30

- **Execução:** 09/12/2026, das 09:41:00 às 10:27:44, com a tag `roteiros-v1.0`.
- **Plano de datas:** os fins de fidelidade das compras do B10 ao B13 foram calculados a partir do momento da execução, como define o roteiro congelado. Nenhum item precisou aguardar.
- **Requisições:** 1.214, todas respondidas em menos de 10 segundos. A aplicação não precisou ser reiniciada.
- **Reposição de dados:** não foi necessária.

| Item | O que é verificado | Verificações que passaram | Pontos | Resultado |
| --- | --- | --- | --- | --- |
| **Etapa 1: Jogadores** | | | **8 de 9** | |
| B01 | Validação do cadastro (V1 a V6 e limites de cada campo) | 38 de 38 | 1,5 de 1,5 | Integral |
| B02 | Códigos de erro e convenções | 10 de 11 | 0 de 1 | Zero |
| B03 | Campos ignorados e `201` com `Location` | 8 de 8 | 1 de 1 | Integral |
| B04 | Edição e alteração de condição | 11 de 11 | 1 de 1 | Integral |
| B05 | Valor de mercado | 12 de 12 | 2 de 2 | Integral |
| B06 | Indicadores e overall | 6 de 6 | 1 de 1 | Integral |
| B07 | Listagem: busca, filtros, ordenação e paginação | 24 de 24 | 1 de 1 | Integral |
| B08 | Exclusão lógica | 6 de 6 | 0,5 de 0,5 | Integral |
| **Etapa 2: Clubes** | | | **1,5 de 1,5** | |
| B09 | Clubes: caixa inicial, nome, sigla e limite de 20 | 14 de 14 | 1,5 de 1,5 | Integral |
| **Etapa 3: Compra** | | | **5 de 5** | |
| B10 | Compra: preço, taxa, limite de 50% do caixa e contrato | 10 de 10 | 1,5 de 1,5 | Integral |
| B11 | Compra recusada | 6 de 6 | 1 de 1 | Integral |
| B12 | Fim da fidelidade | 8 de 8 | 1 de 1 | Integral |
| B13 | Sequência de compras e consulta do clube | 22 de 22 | 1,5 de 1,5 | Integral |
| **Etapa 4: Venda** | | | **3 de 5** | |
| B14 | Multa por fidelidade | 8 de 12 | 0 de 2 | Zero |
| B15 | Venda: lucro, comissão e crédito | 13 de 13 | 2 de 2 | Integral |
| B16 | Venda recusada e recompra | 5 de 5 | 1 de 1 | Integral |
| **Etapa 5: Clubes com elenco** | | | **1 de 1** | |
| B17 | Clubes por patrimônio, filtros de clube e 409 | 9 de 9 | 1 de 1 | Integral |
| **Etapa 6: Histórico e exportação** | | | **2 de 4** | |
| B18 | Histórico e `summary` | 18 de 18 | 2 de 2 | Integral |
| B19 | Exportação CSV | 15 de 16 | 0 de 2 | Zero |
| **Etapa 7: Liga** | | | **4,5 de 4,5** | |
| B20 | Escalação | 13 de 13 | 1,5 de 1,5 | Integral |
| B21 | Partida e duelos | 15 de 15 | 2 de 2 | Integral |
| B22 | Histórico de partidas e classificação | 10 de 10 | 1 de 1 | Integral |
| **Total** | | | **25 de 30** | |

#### B02: valeu zero

Passaram 10 de 11 verificações. Falhou esta:

| Verificação | Pedido | Esperado | Obtido |
| --- | --- | --- | --- |
| B02.07 (V8) | `GET /api/v1/matches/999` | `404` e corpo JSON com `message` | `200`, corpo vazio |

Passaram, entre outras:

- `400` com `message` para corpo que não é JSON válido no `POST /api/v1/players`;
- `404` numa rota inexistente (`GET /api/v1/coaches`) e em jogador e clube inexistentes;
- `Content-Type: application/json; charset=utf-8` nas respostas;
- lista vazia com `200` em `GET /api/v1/matches`, antes da primeira partida.

**Justificativa:** pela V8, recurso inexistente responde `404`. A API respondeu `200` sem corpo para uma partida que não existe. O item só pontua com todas as verificações (barema, seção 3.3). Evidência: saída do script, guardada pela banca, linhas 214 a 233.

#### B14: valeu zero

O script vendeu, pelo clube Tubarões do Norte (id 2), três jogadores comprados no próprio item, todos com valor de mercado igual ao de compra (lucro zero):

- **S1, Vitor Sales:** fidelidade até 09/12/2026, às 09:57; venda às 09:58:02, com a fidelidade já vencida.
- **S2, Henrique Barros:** valor de mercado de 64,00; fidelidade até 08/01/2027, às 16:00; venda às 09:58:31, quando faltavam 30 dias, 6 horas, 1 minuto e 29 segundos.
- **S3, Tiago Menezes:** valor de mercado de 76,00; fidelidade até 27/06/2027, às 09:57; venda às 09:59:10, quando faltavam 199 dias, 23 horas, 57 minutos e 50 segundos.

Passaram 8 de 12 verificações:

| Venda | Campo | Esperado | Obtido | Resultado |
| --- | --- | --- | --- | --- |
| S1 | `remaining_days` | 0 | 0 | passou |
| S1 | `penalty_rate` | 0 | 0 | passou |
| S1 | `penalty` | 0,00 | 0,00 | passou |
| S1 | `contract_status` | `ENCERRADO` | `ENCERRADO` | passou |
| S2 | `remaining_days` | 31 | 30 | falhou |
| S2 | `penalty_rate` | 10 | 5 | falhou |
| S2 | `penalty` | 6,40 (10% de 64,00) | 3,20 | falhou |
| S2 | `contract_status` | `RESCINDIDO` | `RESCINDIDO` | passou |
| S3 | `remaining_days` | 200 | 199 | falhou |
| S3 | `penalty_rate` | 20 | 20 | passou |
| S3 | `penalty` | 10,00 (20% de 76,00 dá 15,20, limitado ao teto de 10,00) | 10,00 | passou |
| S3 | `contract_status` | `RESCINDIDO` | `RESCINDIDO` | passou |

Resposta obtida na S2 (trecho):

```json
{
  "type": "VENDA",
  "value": 64.00,
  "fee": 0.00,
  "penalty": 3.20,
  "profit": 0.00,
  "cash_change": 60.80,
  "purchase_value": 64.00,
  "remaining_days": 30,
  "penalty_rate": 5,
  "contract_status": "RESCINDIDO",
  "club_cash": 213.80
}
```

**Justificativa:** pela RN15, item 1, os dias restantes são arredondados para cima. A API descartou a fração do dia: deu 30 em vez de 31 na S2 e 199 em vez de 200 na S3. Na S2, isso mudou a faixa da multa de 10% para 5%. O `cash_change` da S2 (60,80) não é verificação do B14; o crédito no caixa é conferido no B15, com vendas próprias. Evidência: saída do script, guardada pela banca, linhas 1.402 a 1.488.

#### B19: valeu zero

Passaram 15 de 16 verificações. Falhou a B19.09 (RN18, item 4), no pedido `GET /api/v1/clubs/4/transactions/export?type=VENDA`. O clube Gaviões do Sertão (id 4) tem uma única transação, a compra de `Lucas "Foguete" Prado`; com o filtro `type=VENDA`, não sobra nenhuma.

Esperado, só a linha de cabeçalho:

```text
data_hora;tipo;jogador;valor;taxa_ou_comissao;multa;lucro;variacao_caixa
```

Obtido: arquivo vazio (0 bytes).

Passaram, entre outras:

- `Content-Type: text/csv; charset=utf-8`;
- linha de cabeçalho e linhas na ordem do histórico;
- valores com 2 casas e vírgula decimal, e `lucro` vazio na compra;
- filtros `type` e `player_id`, e respostas `400` e `404` em JSON.

**Justificativa:** pela RN18, item 4, sem transações o arquivo traz só a linha de cabeçalho. A API devolveu um arquivo vazio. Evidência: saída do script, guardada pela banca, linhas 2.010 a 2.094.

#### Amostra de verificações dos itens com pontuação integral

**B05 (valor de mercado):** 5 das 12 verificações. O valor base de cada jogador é o que a API calculou no cadastro (RN06), conferido no B06.

| Jogador | Valor base | Condição | Agilidade | Idade | Desconto por condição | Ajuste por idade | Percentual total | Esperado | Obtido |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Paulo Viana | 114,00 | APTO | 60 | 20 | 0% | +10% | +10% | 125,40 | 125,40 |
| Rafael Tavares | 88,00 | MAL\_CONDICIONADO | 85 | 27 | 7,5% (15% pela metade) | 0% | −7,5% | 81,40 | 81,40 |
| Bruno Siqueira | 46,00 | DOENTE | 20 | 34 | 40% (30% + 10 pontos) | −10% | −50%, limitado a −40% | 27,60 | 27,60 |
| Júlio Prates | 1,50 | DOENTE | 50 | 36 | 30% | −10% | −40% | 1,00 (0,90 sobe para o piso) | 1,00 |
| Sérgio Matos | 9,50 | MAL\_CONDICIONADO | 25 | 22 | 25% (15% + 10 pontos) | 0% | −25% | 7,13 (7,125 arredondado) | 7,13 |

**B06 (overall):** 3 das 6 verificações. Atributos na ordem `pace`, `shooting`, `passing`, `dribbling`, `defending` e `physical`.

| Jogador | Posição | Atributos | Soma dos produtos | Soma ÷ 100 | Esperado | Obtido |
| --- | --- | --- | --- | --- | --- | --- |
| Elias Moura | ZAG | 60, 30, 55, 40, 81, 77 | 7.380 | 73,80 | 74 | 74 |
| Fábio Rocha | ATA | 80, 77, 60, 74, 30, 70 | 7.460 | 74,60 | 75 | 75 |
| Gustavo Leal | LAT | 60, 40, 60, 60, 62, 60 | 6.050 | 60,50 | 61 (meio para cima) | 61 |

No mesmo item, o valor base calculado no cadastro de 3 jogadores do B05:

| Jogador | Overall | Potencial | Idade no cadastro | Parte do overall | Jovem promessa | Esperado | Obtido |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Paulo Viana | 85 | 99 | 20 | 10,00 + 30,00 + 10 × 6,00 = 100,00 | 100,00 × (100 + 14) ÷ 100 | 114,00 | 114,00 |
| Rafael Tavares | 83 | 88 | 27 | 10,00 + 30,00 + 8 × 6,00 = 88,00 | não se aplica | 88,00 | 88,00 |
| Júlio Prates | 43 | 55 | 36 | 3 × 0,50 = 1,50 | não se aplica | 1,50 | 1,50 |

**B10 (limite de 50% do caixa, sem arredondar):** compras do clube Falcões do Agreste (id 3), que começa com 300,00.

| Ordem | Jogador | Valor de mercado | Taxa | Custo total | Caixa antes | Limite | Esperado | Obtido |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Diego Fontes | 105,32 | 5,27 | 110,59 | 300,00 | 150,00 | `200`; caixa de 189,41 | igual |
| 2 | Mateus Cavalcanti | 90,20 | 4,51 | 94,71 | 189,41 | 94,705 | `409`, sem gravar nada | igual |
| 3 | Otávio Rangel | 90,19 | 4,51 | 94,70 | 189,41 | 94,705 | `200`; caixa de 94,71 | igual |

**B13 (sequência de compras):** compras do clube Leões da Serra (id 1), que começa com 300,00.

| Hora | Jogador | Posição | Valor de mercado | Taxa | Custo total | Limite | Caixa depois |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 09:52:05 | Rafael Tavares | GOL | 81,40 | 4,07 | 85,47 | 150,00 | 214,53 |
| 09:52:40 | Bruno Siqueira | ZAG | 27,60 | 0,00 (não passa de 30,00) | 27,60 | 107,265 | 186,93 |
| 09:53:12 | Caio Albuquerque | MEI | 46,00 | 2,30 | 48,30 | 93,465 | 138,63 |
| 09:53:45 | Júlio Prates | ATA | 1,00 | 0,00 | 1,00 | 69,315 | 137,63 |

Consulta `GET /api/v1/clubs/1` às 09:55:20. A resposta trouxe caixa de 137,63, valor do elenco de 156,00 e patrimônio de 293,63, todos iguais ao esperado. O elenco veio nesta ordem:

| Jogador (ordem da RN11) | Valor de mercado | Fim da fidelidade | Dias restantes | % de multa |
| --- | --- | --- | --- | --- |
| Rafael Tavares (GOL) | 81,40 | 09/12/2027, 10:00 | 366 | 20 |
| Bruno Siqueira (ZAG) | 27,60 | 07/02/2027, 10:00 | 61 | 10 |
| Caio Albuquerque (MEI) | 46,00 | 25/12/2026, 10:00 | 17 | 5 |
| Júlio Prates (ATA) | 1,00 | 09/12/2026, 09:54 | 0 | 0 |

A consulta do clube arredondou os dias restantes para cima, como manda a RN15. A venda (B14) não arredondou, porque o cálculo está duplicado no código (ver B2, Regras de negócio).

**B18 (histórico):** clube Tubarões do Norte (id 2), depois das vendas do B14.

- O nome do momento foi mantido: Tiago Menezes foi renomeado pelo `PUT` para Tiago Menezes Filho, e as transações dele continuaram com "Tiago Menezes".
- As transações de jogador excluído foram mantidas: Vitor Sales foi excluído depois da venda, e a compra e a venda dele continuaram no histórico.
- A conciliação do caixa conferiu: 300,00 + (−67,20 − 79,80 − 20,00 + 20,00 + 60,80 + 66,00) = 279,80, igual ao caixa atual.
- O `summary` com `type=VENDA` conferiu: `total_spent` 0,00, `total_received` 146,80, `total_fees` 0,00, `total_penalties` 13,20 e `total_profit` 0,00.

O B18 confere o histórico com os valores que a própria API devolveu em cada operação. A multa da S2 já foi avaliada no B14.

**B21 (partida):** 4 das 15 verificações, com as escalações do roteiro: Corujas do Cabo (id 5), mandante, e Falcões do Agreste (id 3), visitante, as duas no `2-1-1`. No Corujas do Cabo, o LAT estava `MAL_CONDICIONADO`.

| Verificação | Pedido | Esperado | Obtido |
| --- | --- | --- | --- |
| B21.01 | `POST /api/v1/matches`, corpo `{"home_club_id": 5, "away_club_id": 3}` | `201`, `Location: /api/v1/matches/1`, placar 1 × 2 e `result` `VISITANTE` | igual |
| B21.04 | duelo 3 da mesma partida: drible 74 do LAT `MAL_CONDICIONADO` contra defesa 63 | `value` 63 no atacante (74 × 0,85 = 62,9) e `goal: false` (duelo empatado) | igual |
| B21.09 | `POST /api/v1/matches` com `home_club_id` igual a `away_club_id` | `400`, sem gravar nada | igual |
| B21.11 | `POST /api/v1/matches` com o visitante sem escalação completa | `409`, sem gravar nada | igual |

### B2. Qualidade do código do backend: 7 de 10

| Critério | Nível | Pontos |
| --- | --- | --- |
| Camadas | Não atende | 0 de 2 |
| Regras de negócio | Atende em parte | 1 de 2 |
| Validação e erros | Atende | 2 de 2 |
| Consistência dos dados | Atende | 2 de 2 |
| Segurança e configuração | Atende | 1 de 1 |
| Código morto e padrão | Atende | 1 de 1 |
| **Total** | | **7 de 10** |

- **Camadas:** 3 ocorrências, o que fica em "não atende" (3 ou mais):
  - a rota da exportação do histórico consulta o banco direto no controlador;
  - a rota da lista de clubes calcula o patrimônio (RN11) no controlador para ordenar os clubes;
  - a rota da consulta do jogador por id consulta o banco direto no controlador, sem passar pelo serviço.
- **Regras de negócio:** há 1 cálculo duplicado, o da multa (dias restantes e percentual, RN15).
  - Ele aparece na consulta do clube, que arredonda os dias para cima, e na venda, que descarta a fração do dia.
  - Os outros 5 cálculos (valor de mercado, overall, taxa, comissão e placar da partida) estão cada um em um único lugar, na camada de regras de negócio.
- **Validação e erros:** os 18 endpoints que recebem corpo, query params ou id validam a entrada por mecanismo declarado:
  - esquemas de validação aplicados a todas as rotas, mais uma validação própria para os ids da URL;
  - as recusas passam por um tratamento central de erros;
  - a busca por stack trace nas 1.214 respostas do B1 não achou nenhuma ocorrência.
- **Consistência dos dados:** compra, venda, partida (com o placar e os 6 duelos), escalação (com a formação e os 5 titulares) e alteração de condição para `DOENTE` (com a saída da escalação) rodam, cada uma, numa transação do banco.
- **Segurança e configuração:** as 4 práticas estão presentes:
  - consultas pelo ORM, sem SQL montado com valores recebidos;
  - senha do banco lida de variável de ambiente;
  - CORS restrito à origem do frontend, lida de variável de ambiente;
  - nenhuma credencial real; o `.env.example` traz só a senha do banco local.
- **Código morto e padrão:** a busca por código comentado e por arquivos, funções e variáveis sem uso no backend não achou ocorrência, e os nomes seguem as convenções da linguagem.

### B3. Banco de dados: 5 de 6

| Critério | Nível | Pontos |
| --- | --- | --- |
| Criação reprodutível | Atende | 2 de 2 |
| Estrutura | Atende em parte | 1 de 2 |
| Restrições | Atende | 2 de 2 |
| **Total** | | **5 de 6** |

- **Criação reprodutível:** o README do backend, item 2, cria o banco com `docker compose up -d db` e `npx prisma migrate deploy` e o recria do zero com `npx prisma migrate reset --force`.
  - Os comandos funcionaram na preparação e nas duas recriações, às 09:40 e às 10:31.
  - As 3 migrations estão versionadas no repositório.
- **Estrutura:** há 1 desvio. A coluna `duelos_partida.valor_defesa` foi criada com o nome `valor_defensor`. As 7 tabelas e as demais colunas, chaves primárias, chaves estrangeiras e tipos de moeda (`NUMERIC`) conferem com "3. Estrutura de tabelas".
- **Restrições:** todas estão garantidas no banco, e não há coluna de valor calculado:
  - índice único em `clubes.nome_normalizado`, coluna preenchida pela aplicação com o nome com espaços normalizados e em minúsculas;
  - `UNIQUE` em `clubes.sigla`;
  - `UNIQUE` em `escalacoes.jogador_id`.

Conferência das unicidades, às 12:40, no banco recriado depois dos roteiros. Cada inserção partiu de uma linha criada antes pela API:

| Inserção direta | Esperado | Obtido |
| --- | --- | --- |
| Clube "águias fc" (`nome_normalizado` "águias fc", sigla nova AGF), com "Águias FC" já cadastrado | recusada | recusada pelo índice único do nome |
| Clube "Aguias FC" (`nome_normalizado` "aguias fc", sigla nova AGI) | aceita | aceita |
| Sigla AGU repetida, com nome novo "Gaviões do Litoral" | recusada | recusada pelo índice único da sigla |
| Jogador 14 numa segunda escalação, com a primeira já gravada | recusada | recusada |

### B4. README e histórico do Git do backend: 1,5 de 2

| Critério | Nível | Pontos |
| --- | --- | --- |
| README do backend | Atende em parte | 0,5 de 1 |
| Histórico do Git | Atende | 1 de 1 |
| **Total** | | **1,5 de 2** |

Itens do README conferidos (1 e 3 a 8; o item 2 conta só em B3):

| Item | Situação | Evidência |
| --- | --- | --- |
| 1. Pré-requisitos | correto | Node.js 22, PostgreSQL 16 (imagem `postgres:16-alpine`) e Docker 27 |
| 3. Instalar e executar | correto | comandos executados como escritos; origem `http://localhost:3000`; arquivo de trava de dependências versionado |
| 4. Variáveis de ambiente | **incorreto** | a variável `CORS_ORIGIN`, lida pelo backend, não está no `.env.example` nem no README |
| 5. Estrutura e bibliotecas | correto | pastas descritas; as 9 bibliotecas além da stack, cada uma com o motivo |
| 6. Decisões e premissas | correto | decisões sobre o que o enunciado não definiu (mensagens de erro em português e ordem das validações de negócio) |
| 7. Funcionalidades não implementadas | correto | "Nenhuma" |
| 8. Uso de inteligência artificial | correto | ferramentas, onde, como e por quê, e o que foi aceito, alterado ou descartado |

- **README do backend:** 1 item incorreto, o 4. Fica em "atende em parte".
- **Histórico do Git:** 34 commits alteram `backend/`, todos dentro do prazo, e foram enviados (push) em 7 dias diferentes: 24/11, 25/11, 26/11, 28/11, 30/11, 01/12 e 03/12. Só 4 das 34 mensagens são genéricas ("fix", "ajustes", "wip" e "update"), menos da metade.

### B5. Diferenciais técnicos do backend: 2 de 2

| Diferencial | Verificação | Resultado | Pontos |
| --- | --- | --- | --- |
| Testes automatizados | `npm test` (Jest) terminou sozinho em 38 s, com 41 testes e nenhuma falha; um dos testes confere o valor de mercado | passa | 0,5 de 0,5 |
| Docker e Docker Compose | `docker compose --profile full up -d --build` subiu interface, API e banco em 9 min 40 s; a lista de jogadores abriu em `http://localhost:8080`, a URL informada no README | passa | 0,5 de 0,5 |
| Documentação interativa | `http://localhost:3000/api/docs` abriu com os 19 endpoints de "2. Endpoints" | passa | 0,5 de 0,5 |
| Registro de logs | depois de `GET /api/v1/players`, a saída mostrou uma única linha, `[Nest] 4211 - 09/12/2026, 11:52:03 LOG [HTTP] GET /api/v1/players 200`, gerada pelo Logger do NestJS | passa | 0,5 de 0,5 |
| Lint e formatação | `npm run lint` (ESLint) e `npm run format:check` (Prettier) terminaram sem erros e sem alterar arquivos | passa | 0,5 de 0,5 |

Os diferenciais somam 2,5 pontos, limitados ao máximo de 2.

## 7. Frontend

### F1. Roteiro da interface: 25 de 30

- **Execução:** 09/12/2026, das 10:31:30 às 11:19:00, no Chrome, numa janela de 1366 × 768, com o banco recriado e a carga inicial do roteiro feita pela API.
- **Plano de datas:** os fins de fidelidade foram calculados a partir do momento da execução.
- **Evidências:** vídeo `C07-F1.mp4` e registro de rede `C07-F1.har`. Os trechos abaixo são posições no vídeo.

| Item | O que é verificado pela tela | Trecho do vídeo | Pontos | Resultado |
| --- | --- | --- | --- | --- |
| F01 | Tabela de jogadores e paginação de 10 por página | 00:01:10 a 00:03:40 | 2 de 2 | Integral |
| F02 | Busca, filtros combinados e ordenações | 00:03:40 a 00:09:15 | 2 de 2 | Integral |
| F03 | Excluir com confirmação | 00:09:15 a 00:11:30 | 1 de 1 | Integral |
| F04 | Cadastro, edição e alteração de condição | 00:11:30 a 00:17:05 | 2 de 2 | Integral |
| F05 | Clubes: listagem por nome e criação | 00:17:05 a 00:18:35 | 2 de 2 | Integral |
| F06 | Compra e resultado | 00:18:35 a 00:24:05 | 3 de 3 | Integral |
| F07 | Página do clube e clubes por patrimônio | 00:24:05 a 00:26:35 | 2 de 2 | Integral |
| F08 | Venda e resultado | 00:26:35 a 00:30:45 | 3 de 3 | Integral |
| F09 | Histórico com sinais e filtros | 00:30:45 a 00:33:55 | 3 de 3 | Integral |
| F10 | Totais do `summary` com filtro | 00:33:55 a 00:35:25 | 2 de 2 | Integral |
| F11 | Exportar CSV com os filtros | 00:35:25 a 00:36:55 | 1 de 1 | Integral |
| F12 | Escalação na página do clube | 00:36:55 a 00:40:10 | 2 de 2 | Integral |
| F13 | Partida e duelos | 00:40:10 a 00:44:20 | 0 de 3 | Zero |
| F14 | Histórico de partidas e classificação | 00:44:20 a 00:47:30 | 0 de 2 | Zero |
| **Total** | | | **25 de 30** | |

#### F13: valeu zero

| Passo | Esperado | Obtido |
| --- | --- | --- |
| Escolher Corujas do Cabo como mandante e Falcões do Agreste como visitante e jogar (HAR, pedido 341: `POST /api/v1/matches`) | resultado com o placar e os 6 duelos devolvidos pela API | só o placar, 1 × 2 (vídeo, 00:41:35) |
| Abrir a mesma partida no histórico (HAR, pedido 344: `GET /api/v1/matches/1`) | os 6 duelos, com atacante, defensor, atributos, valores e gol | a resposta trazia os 6 duelos, mas a tela mostrou só o placar (vídeo, 00:42:50) |
| Jogar com o visitante sem escalação completa (HAR, pedido 349) | o `message` da API | igual |

- **Justificativa:** o F13 exige o placar e os 6 duelos devolvidos pela API. A tela mostrou só o placar.
- **Revisão do zero:** antes de fechar a nota, o item foi revisto pelo vídeo e pelo HAR, e o zero foi mantido.

#### F14: valeu zero

| Passo | Esperado | Obtido |
| --- | --- | --- |
| Abrir a classificação depois das 3 partidas do roteiro (HAR, pedido 356: `GET /api/v1/standings`) | a ordem devolvida pela API: Leões da Serra (3 pontos, saldo +1), Corujas do Cabo (3 pontos, saldo 0) e Falcões do Agreste (3 pontos, saldo −1) | Corujas do Cabo, Falcões do Agreste e Leões da Serra, em ordem alfabética (vídeo, 00:45:10) |
| Filtrar o histórico de partidas pelo Falcões do Agreste (HAR, pedido 359: `GET /api/v1/matches?club_id=3`) | 2 partidas, da mais recente para a mais antiga | igual |

- No código, a tela reordena a lista recebida por pontos e, no empate, pelo nome, ignorando o saldo de gols.
- **Justificativa:** o F14 exige a classificação na ordem devolvida por `GET /standings`.
- **Revisão do zero:** antes de fechar a nota, o item foi revisto pelo vídeo e pelo HAR, e o zero foi mantido.

#### Amostra de itens com pontuação integral

- **F04:**
  - A tela abriu a edição de Wagner Lins (id 12), mudou a agilidade e enviou `PUT /api/v1/players/12` (pedido 61), que respondeu `200`.
  - A tabela mostrou os dados devolvidos pela API, sem recarregar a página.
- **F06:**
  - Compra de Renan Duarte (MEI, valor base calculado de 58,00, MAL\_CONDICIONADO, agilidade 50, 25 anos) pelo Leões da Serra, com caixa de 300,00.
  - O fim da fidelidade foi digitado como 25/01/2027, 18:00, e enviado como `2027-01-25T18:00-03:00` (pedido 140).
  - O resultado mostrou: valor 49,30, taxa 2,47, custo total 51,77, fim da fidelidade 25/01/2027 18:00 e novo caixa 248,23.
  - Depois disso, a tabela mostrou o clube LDS no jogador, o filtro pelo clube o encontrou, e o filtro "só livres" deixou de mostrá-lo.
- **F08:** venda de Renan Duarte às 11:06:30.
  - A tela mostrou: valor de compra 49,30, valor de venda 49,30, dias restantes 47, multa 4,93, lucro 0,00, comissão 0,00, crédito 44,37 e novo caixa 292,60.
  - Pela RN15, seriam 48 dias (faltavam 47 dias, 6 horas, 53 minutos e 30 segundos). A tela mostrou o que a API devolveu, e o erro da API já foi avaliado no B14, por isso o item da tela não perde ponto (barema, seção 3.4).
- **F10:** os cinco totais abaixo da tabela foram iguais aos do `summary` da resposta, sem filtro (pedido 199) e com `type=VENDA` (pedido 201).

### F2. Qualidade do código do frontend: 7 de 10

| Critério | Nível | Pontos |
| --- | --- | --- |
| Componentes | Atende em parte | 1 de 2 |
| Acesso à API | Atende | 2 de 2 |
| Atualização e regras | Atende | 2 de 2 |
| Formulários | Atende em parte | 1 de 2 |
| Código morto e padrão | Atende em parte | 1 de 2 |
| **Total** | | **7 de 10** |

- **Componentes:** 1 componente duplicado, a tabela.
  - Um componente de tabela compartilhado é usado nas telas de jogadores, de clubes e do clube.
  - A tela do histórico de partidas monta a própria tabela, com o cabeçalho, as linhas e os estados de carregamento, vazio e erro, em vez de usar o componente compartilhado.
  - O campo de formulário e as mensagens também vêm de componentes compartilhados.
- **Acesso à API:** todas as chamadas estão numa camada própria, usada pelos hooks de dados. A busca por chamadas HTTP diretas nos componentes não achou nenhuma ocorrência.
- **Atualização e regras:**
  - Nas gravações do F1 e do F3, as 9 ações atualizaram a tela pela API, sem recarregar a página. No código, os hooks de dados buscam de novo o que cada ação altera.
  - Nenhum valor devolvido pela API é recalculado na tela. O custo total da compra soma valor e taxa, o que é permitido.
- **Formulários:** o formulário de escalação deixa salvar sem um titular em cada uma das 5 vagas da formação; a recusa fica só para a API.
  - Os outros 6 formulários validam o que o barema lista e enviam as datas com `-03:00`.
- **Código morto e padrão:** 2 arquivos, o que fica em "atende em parte" (1 a 5 arquivos): código comentado na página do clube (15 linhas) e uma função de formatação de percentual que nada usa. Um hook usado só pelos testes não conta como código sem uso.
- **Sem dupla penalização:** os defeitos que zeraram o F13 e o F14 não foram contados de novo em F2 nem em F3.

### F3. Usabilidade e feedback: 4 de 6

Sessão gravada de 09/12/2026, das 11:30 às 12:05: banco recriado, rede desacelerada no perfil registrado na ata e navegação pela própria interface. Evidências: `C07-F3.mp4` e `C07-F3.har`.

| Critério | Nível | Pontos |
| --- | --- | --- |
| Mensagens | Atende em parte | 1 de 2 |
| Estados das telas | Atende em parte | 1 de 2 |
| Apresentação | Atende | 2 de 2 |
| **Total** | | **4 de 6** |

- **Mensagens:** 2 das 9 ações mostraram mensagem genérica na recusa, em vez do `message` da API, o que fica em "atende em parte":
  - criar clube (`409`, sigla repetida, 00:12:31): "Não foi possível salvar.";
  - comprar (`409`, custo acima do limite de 50% do caixa, 00:14:52): "Não foi possível salvar."

  As outras 7 ações mostraram mensagem de sucesso e, nas recusas, o `message` da API. Nas 9, o clique duplo gerou um só pedido (HAR). Na alteração de condição (`409`, de DOENTE para APTO, 00:08:05), por exemplo, a tela mostrou "Jogador DOENTE não pode passar direto para APTO."
- **Estados das telas:** a tela de histórico de partidas não mostra o estado de lista vazia. Com o banco recém-recriado, ela mostra só o cabeçalho da tabela (00:02:15). As outras 5 telas de lista mostram carregamento, lista vazia e erro.
- **Apresentação:** as 6 telas mostram valores com 2 casas e vírgula decimal e datas no horário de Brasília.

### F4. README e histórico do Git do frontend: 1 de 2

| Critério | Nível | Pontos |
| --- | --- | --- |
| README do frontend | Atende em parte | 0,5 de 1 |
| Histórico do Git | Atende em parte | 0,5 de 1 |
| **Total** | | **1 de 2** |

- **README do frontend:** os itens 1, 3 e 4 estão corretos; o item 4 informa a variável com a origem da API, que está no `.env.example` do frontend. O item 5 está incorreto: a lista de bibliotecas não traz a `dayjs`, que está nas dependências do frontend e só aparece em "Decisões e premissas". Com 1 item incorreto, fica em "atende em parte".
- **Histórico do Git:** 21 commits alteram `frontend/`, mas foram enviados (push) em só 2 dias, 02/12 e 03/12. Por ter envios em menos de 3 dias, fica em "atende em parte". Só 3 das 21 mensagens são genéricas.

### F5. Diferenciais de interface: 2 de 2

| Diferencial | Verificação | Resultado | Pontos |
| --- | --- | --- | --- |
| Responsividade | Com 375 px, a lista de jogadores e a página do clube, com o histórico, não tiveram rolagem horizontal da página; as tabelas rolam no próprio quadro, e as ações continuaram acessíveis (vídeo `C07-F3.mp4`, 00:27:10 a 00:31:00) | passa | 1 de 1 |
| Testes no frontend | `npm test` (`vitest run`) terminou sozinho em 6 s, com 9 testes de componente e nenhuma falha | passa | 1 de 1 |
| Lint e formatação | o README do frontend não informa comandos de lint nem de formatação | não passa | 0 de 0,5 |

Os diferenciais somam 2 pontos, o máximo.

## 8. Comunicação do resultado

- Esta ficha é enviada ao candidato com o resultado, em 18/12/2026, junto com os nomes dos membros da banca.
- Os anexos são os vídeos e os arquivos HAR.

## 9. Evidências e integridade

| Evidência | Arquivo | SHA-256 |
| --- | --- | --- |
| Cópia espelho do repositório | `C07-repositorio.tar.gz` | `4ad82b22dfbdb5fd63e24c2369438bbda18fedc18de08efe0bc497a371163cdc` |
| Histórico de envios (push) | `C07-envios.json` | `bd6f72d1db5c3e7b1218644e2cc6c17fbc45ed2c7b7ab06b37f4e1d52f8b57b9` |
| Vídeo do F1 | `C07-F1.mp4` | `0a96b480366df454eab55ede53a762c63bc3fc8d0447c7a8476a0b98ad9da2f7` |
| Registro de rede do F1 | `C07-F1.har` | `778214ed6bbca6587c3f55ead0730253877a76ba245c43757e5d1fea2dda8923` |
| Vídeo da sessão do F3 e dos diferenciais | `C07-F3.mp4` | `69582ccc7c2226bbe0881a6182fe101047e77d247e232540db0becb4ab7a3287` |
| Registro de rede da sessão do F3 | `C07-F3.har` | `46bad3b7ca598692df1a5f78d08fcb52a2dbc06317e939dbc9b1a0483462c2e8` |
| Vídeo do diferencial de Docker | `C07-docker.mp4` | `76ff08847bc5e6b07b6d82eee784035a1b887a1b337073036ed9c58ce064ea18` |
| Ficha de avaliação assinada | `C07-ficha.pdf` | `4a0cffe958f2844acf796db3b15ecb67f1e049badc636a5267973a811b79ff57` |

## 10. Registro

| Função | Data | Registro |
| --- | --- | --- |
| Avaliador 1 | 11/12/2026 | ficha entregue ao RH; zeros do F13 e do F14 revistos pelo vídeo e pelo HAR; declaração de impedimento assinada; leitura sem assistentes de IA |
| Coordenação | 15/12/2026 | ficha conferida: limite de B5 e cálculo da nota final |
| RH | 15/12/2026 | identificação do código C-07 depois de fechadas todas as notas; declarações renovadas, sem impedimento |
