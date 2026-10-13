# Barema e processo de correção

Estudo de Caso da vaga SENAI/PE – CÓD. 237 DESENVOLVEDOR I (FULLSTACK). Este documento define como a nota é calculada, como a correção é feita e quais controles a banca segue. Ele vale igualmente para todos os candidatos e complementa o enunciado ([README.md](README.md)).

## 1. Princípios da correção

- **Mesmas condições para todos:** mesmo ambiente, mesmo roteiro, mesmos dados e mesma ordem de verificação para todos os candidatos.
- **Critérios definidos antes da correção:** o enunciado, este barema, os roteiros e os dados de teste são fechados antes do fim do prazo de entrega e não mudam durante a correção. A única exceção é o erro nos roteiros (seção 3.3), corrigido para todos.
- **Itens objetivos:** os roteiros da API e da interface valem a pontuação integral ou zero; não há pontuação parcial dentro de um item.
- **Rubricas mensuráveis:** os critérios de leitura têm limites numéricos, e cada projeto é corrigido por um avaliador.
- **Identificação reduzida:** os avaliadores corrigem pelo código do candidato, sem nome nem e-mail, e declaram não ter impedimento (seção 3.7).
- **Evidência para cada nota:** todo item tem evidência registrada (saída do script, gravação da tela, registro de rede ou trecho do código) e justificativa na ficha de avaliação.
- **Transparência:** o candidato recebe a ficha com o resultado esperado e o obtido, a evidência (anexada ou indicada) e a justificativa de cada item, e pode pedir no recurso as evidências que ficam com a banca (seção 3.6).

## 2. Composição da nota

A nota vai de 0 a 10. O backend vale até 5,0 e o frontend, até 5,0.

| Parte | Critério | Como é avaliado | Pontos | Na nota |
| --- | --- | --- | --- | --- |
| Backend | B1. Roteiro da API | Script automatizado | 30 | 3,0 |
| Backend | B2. Qualidade do código | Leitura do código, com rubrica | 10 | 1,0 |
| Backend | B3. Banco de dados | Leitura do código, com rubrica | 6 | 0,6 |
| Backend | B4. README e histórico do Git | Leitura do repositório, com rubrica | 2 | 0,2 |
| Backend | B5. Diferenciais técnicos | Verificação de cada diferencial | 2 | 0,2 |
| **Backend** | | | **50** | **5,0** |
| Frontend | F1. Roteiro da interface | Execução na tela | 30 | 3,0 |
| Frontend | F2. Qualidade do código | Leitura do código e uso da interface, com rubrica | 10 | 1,0 |
| Frontend | F3. Usabilidade e feedback | Uso da interface, com rubrica | 6 | 0,6 |
| Frontend | F4. README e histórico do Git | Leitura do repositório, com rubrica | 2 | 0,2 |
| Frontend | F5. Diferenciais de interface | Verificação de cada diferencial | 2 | 0,2 |
| **Frontend** | | | **50** | **5,0** |
| **Total** | | | **100** | **10,0** |

- **Nota final:** soma dos pontos ÷ 10 (ex.: 76,5 pontos → 7,65). Como todo critério pontua em múltiplos de 0,5, a nota tem no máximo duas casas decimais.
- **Aprovação:** nota final igual ou maior que **7,0**, com pelo menos **2,5 no backend** e **2,5 no frontend**. Os critérios de aprovação não mudam depois do envio do enunciado, mesmo que nenhum candidato os atinja; nesse caso, o resultado é publicado sem aprovados.
- **Empate:** não há desempate nem sorteio; candidatos com a mesma nota final ficam na mesma posição.
- **Eliminação:** segue o regulamento e independe da nota. Nesta etapa, a banca aplica a eliminação somente nestas situações:
  1. e-mail de entrega recebido depois do prazo, sem outro recebido no prazo (o e-mail recebido depois do prazo é desconsiderado quando há outro no prazo);
  2. repositório inacessível sem login no momento da cópia (seção 3.1), por estar privado, removido ou com o link errado;
  3. hash ausente no e-mail, ou que não identifica um commit alcançável a partir dos branches e tags registrados na cópia (seção 3.1); o commit não precisa estar no branch principal. Hash abreviado, ou dentro do link do commit, é falha de formato e não elimina, desde que identifique um único commit enviado (push) até o fim do prazo, segundo o histórico de envios; caso contrário, conta como hash que não existe;
  4. commit informado sem nenhuma das pastas `frontend/` e `backend/` na raiz do repositório (o nome é comparado sem diferenciar maiúsculas e minúsculas);
  5. tecnologia fora da 🧭 Stack obrigatória do enunciado, inclusive banco não aceito como banco da aplicação (como SQLite) e rotas de API, Route Handlers ou Server Actions do Next.js que acessem o banco ou calculem o que a API devolve, em vez de repassar a chamada ao backend (validar um formulário antes de repassá-lo não elimina);
  6. cópia comprovada de código de outro candidato, apurada como descrito abaixo.

  Outras falhas de formato da entrega (como assunto fora do modelo, falta da cópia para o RH ou anexo enviado junto com o link) não eliminam. O e-mail enviado de endereço diferente daquele em que o candidato recebe as comunicações do RH sobre a vaga é desconsiderado (enunciado, “📦 Como enviar sua entrega”). Cada eliminação é registrada na ata, com a evidência e a justificativa, e só vale com duas pessoas de acordo: no item 1, o RH e a coordenação; nos demais, o avaliador do projeto e outro membro da banca. A eliminação é comunicada com o resultado.
- **Cópia:** a banca compara todos os projetos entre si com uma ferramenta de detecção de similaridade de código, executada localmente, com o nome, a versão, a configuração e o limite de similaridade registrados em ata e enviados ao RH e ao jurídico antes do fim do prazo. Código de bibliotecas, arquivos gerados por ferramentas e trechos do enunciado ficam fora da comparação. Cada par acima do limite é analisado por um avaliador. A cópia só é considerada comprovada quando ele aponta na ata trechos não triviais iguais, ou diferentes só em nomes, formatação ou ordem, com coincidências arbitrárias (como comentários, mensagens de erro ou defeitos iguais) que não venham do enunciado, de bibliotecas nem de arquivos gerados por ferramentas, e outro membro da banca confirma, como em toda eliminação. Semelhança explicada pelo uso declarado de IA, por bibliotecas ou pelo enunciado não caracteriza cópia por si só. Antes da decisão, o RH envia a cada candidato do par o relatório da ferramenta e os trechos semelhantes, sem identificar o outro candidato, e ele tem 2 dias úteis para se manifestar por escrito. A autoria não é decidida pelas datas dos commits, que podem ser alteradas por quem faz o commit; a banca usa evidências que o candidato não controla, como o histórico de envios (push) da plataforma. Comprovada a cópia, é eliminado quem copiou; se não for possível identificar quem copiou, decide-se conforme o regulamento.
- **Entrevista:** esta nota não inclui entrevista, que é uma etapa separada, com critérios próprios. São convocados para ela os 10 primeiros colocados entre os aprovados e todos os empatados na 10ª posição.
- **Prevalência:** em caso de divergência entre documentos, vale esta ordem: regulamento (fora da seção 4 e do barema), erratas, este barema (para a pontuação) e o enunciado (para os requisitos); o glossário, o mockup e o exemplo de ficha de avaliação são informativos.

## 3. Processo de correção

### 3.1 Versão corrigida

- É corrigido o commit cujo hash completo (40 caracteres) foi informado no e-mail de entrega, no repositório indicado. Commits posteriores a ele não são considerados.
- Às 12h (horário de Brasília) do dia útil seguinte ao fim do prazo, a banca registra, para todos os repositórios ao mesmo tempo, os branches e tags e o commit de cada um (`git ls-remote`). Em seguida, faz uma cópia espelho de cada repositório (`git clone --mirror`), compacta a cópia e registra em ata o SHA-256 do arquivo. Junto com a cópia, salva o histórico de envios (push) do repositório, como a plataforma o mostra.
- O commit informado precisa ser alcançável a partir de um dos branches ou tags registrados. Como o hash fixa o conteúdo, o envio (push) feito entre o fim do prazo e a cópia não muda o que é corrigido; nos dias de envio (B4 e F4), só conta o que foi feito até o fim do prazo.
- Se a cópia falhar, a banca tenta de novo em três momentos diferentes nas 24 horas seguintes e registra as tentativas em ata; nas novas tentativas, os branches e tags são registrados no momento da cópia. A indisponibilidade da plataforma é conferida na página de status dela, salva na ata; se a plataforma seguir fora do ar depois das três tentativas, a banca tenta de novo a cada 24 horas até conseguir. Só há eliminação (seção 2) se, nas três tentativas, a plataforma estiver no ar e o repositório não puder ser acessado sem login.
- Toda a correção usa essa cópia. Mudanças posteriores no repositório (torná-lo privado, apagá-lo ou alterar o histórico) não mudam a correção.

### 3.2 Ambiente e preparação

- Cada candidato é corrigido numa máquina virtual própria, criada a partir da mesma imagem, numa rede separada da rede interna do Instituto e sem credenciais da banca, exceto um acesso ao Docker Hub só para downloads: **Ubuntu 24.04 LTS** (amd64), 4 vCPUs, 8 GB de memória, 40 GB de disco livre, Docker Engine com Docker Compose v2 utilizável sem `sudo`, fuso horário `America/Sao_Paulo`, idioma `pt_BR.UTF-8`, relógio sincronizado pela internet (NTP), Google Chrome estável e acesso à internet. As versões ficam na ata.
- Antes da preparação, a banca instala só os runtimes e os gerenciadores oficiais pedidos nos pré-requisitos do README (Node.js com npm, Java com Maven ou Gradle, Python com pip), nas versões pedidas e dentro das permitidas pelo enunciado. Se o README não indicar a versão de um runtime, ou indicar versão fora das permitidas, a banca usa a versão permitida mais próxima da pedida ou, sem versão pedida, a mais recente permitida lançada até o envio do enunciado, e isso não elimina por si só. O banco e as demais ferramentas (como pnpm, Yarn ou Poetry) são instalados ou iniciados pelos comandos do próprio README, dentro do tempo da preparação.
- A banca executa só os comandos do README da raiz e dos READMEs de `backend/` e `frontend/` para os quais ele aponta, copiados literalmente e na ordem indicada. A única ação além deles é copiar o `.env.example` para `.env`, sem alterar valores, quando o README mandar. Havendo caminhos alternativos, a banca segue o primeiro aplicável ao Ubuntu 24.04. Pedido de senha do `sudo` é respondido com a senha do usuário da máquina virtual, e outras perguntas interativas recebem a resposta padrão (tecla Enter); comando com valor a preencher sem valor indicado no README conta como comando que falhou. A banca não altera código, configuração nem dependências. Comando que dependa de recurso controlado pelo candidato (imagem própria, submódulo ou serviço hospedado) não é executado; imagem pública de terceiro é usada. Comandos indicados como opcionais (como a carga de dados de exemplo) não são executados. Comando que fica em execução (como o servidor da API ou do frontend) continua rodando, e os seguintes são executados em outro terminal.
- A preparação tem até **30 minutos**, contados do primeiro comando. Se um comando falhar por instabilidade de rede, ele é repetido uma única vez, dentro desse tempo.
- A tela é gravada durante toda a preparação; o vídeo fica com a banca, com o SHA-256 em ata, e não é anexado à ficha. Preparação que falhar é revista pelo vídeo antes de a nota ser fechada; se a revisão mostrar comando executado de forma diferente do README, a preparação é refeita do zero. Se a preparação falhar por problema de infraestrutura da banca (como queda de energia, de internet ou da máquina virtual) ou por falha de serviço externo de que ela depende (registro de pacotes ou de imagens, como npm, Maven Central, PyPI ou Docker Hub), com a mensagem de erro gravada no vídeo e registrada em ata, ela é refeita do zero em outro horário.
- O backend está no ar quando a origem da API responde a requisições HTTP, com qualquer código; o frontend, quando a URL informada abre uma página no Chrome. Com a aplicação no ar, os roteiros são executados mesmo que parte dos endpoints ou das telas falhe, e cada item vale pelo próprio resultado. O script usa a origem da API informada no README, acrescida de `/api/v1`; se a origem vier com `/api/v1`, o sufixo não é repetido. Se o README informar só a porta, a banca usa `http://localhost:<porta>`; se informar mais de uma origem, vale a primeira do passo de execução; sem origem nem porta, a banca usa a origem que o comando de execução mostrar na tela e, se ele não mostrar, o roteiro da API vale zero. As mesmas regras valem para a URL do frontend e o roteiro da interface.
- O banco é **recriado do zero** antes do roteiro da API e antes do roteiro da interface, pelos comandos de recriação do README, para que um roteiro não interfira no outro. Se o README não trouxer como recriar, a banca restaura o instantâneo (snapshot) da máquina virtual tirado ao fim da preparação, com o banco recém-criado. Se a recriação parar a aplicação, a banca executa de novo os comandos de execução do README, e a origem da API tem até 10 minutos para responder; se a recriação falhar, a banca restaura o instantâneo da preparação.
- O instantâneo tirado ao fim da preparação é guardado até a divulgação do resultado do estudo de caso, e toda nova execução (erro nos roteiros) parte dele, sem nova preparação; a máquina virtual é descartada depois dessa divulgação. Antes de encerrar cada sessão, o avaliador confere se a saída do script, os vídeos e os arquivos HAR foram salvos fora da máquina virtual e registra o SHA-256 de cada um; se faltar evidência, os itens afetados são executados de novo, com o banco recriado.
- Se o backend não subir no tempo (a origem da API não responde a nenhuma requisição), valem zero B1, F1, F3 e os diferenciais que dependem da aplicação no ar (documentação interativa e logs, em B5; responsividade, em F5). Se só o frontend não subir, valem zero F1, F3 e a responsividade. Os demais critérios continuam sendo avaliados, inclusive o diferencial de Docker, que sobe a aplicação pelo próprio comando (seção 3.5).

### 3.3 Roteiro da API (B1)

- Executado por script automatizado, o mesmo e na mesma versão para todos, com dados próprios da banca. Os exemplos do enunciado não são usados como dados de teste.
- O script só verifica o que o enunciado define, e cada verificação cita a regra que a fundamenta. Nos pontos deixados à decisão do candidato, qualquer escolha coerente é aceita, e nenhuma verificação depende dela. Nenhum pedido combina dois erros (V9).
- O roteiro congelado define a carga inicial (os dados que o script cadastra pela API antes de cada etapa) e o plano de datas: as datas são calculadas a partir do momento da execução, e alguns itens aguardam alguns minutos (por exemplo, o fim de uma fidelidade curta).
- Os itens são executados na ordem da tabela da seção 4. Um item vale a pontuação integral somente se **todas** as suas verificações passarem; caso contrário, vale zero.
- **Recusa:** é aceita quando tem o código HTTP previsto, traz um objeto JSON com `message` (texto não vazio) e não grava nada, o que o script confere com consultas pela API. O texto da mensagem não é avaliado. O cabeçalho `Content-Type` das respostas só é conferido no B02 e no B19; nos demais itens, o corpo é lido como JSON mesmo sem ele.
- **Comparações:** cabeçalhos são comparados pelo significado: nomes sem diferenciar maiúsculas e minúsculas, `Content-Type` das respostas JSON com ou sem `charset=utf-8` e, na exportação, `text/csv` com ou sem `charset` (RN18), e `Location` como caminho a partir da raiz ou URL absoluta. Números são comparados pelo valor (`40`, `40.0` e `40.00` são iguais), e campos adicionais nas respostas são ignorados.
- **Pedidos do script:** usam HTTP/1.1, o cabeçalho `Accept: */*` e os caminhos exatamente como no enunciado, sem barra no final. Os pedidos com corpo levam `Content-Type: application/json`; os demais vão sem corpo. O script não segue redirecionamentos: uma resposta 3xx conta como a resposta do pedido.
- **Reposição de dados:** se um item que prepara dados para os seguintes falhar, o script cria esses dados pela API, com pedidos simples e válidos previstos no roteiro (item 5.6.4 do regulamento), e segue. Se a reposição também falhar, os itens que dependem desses dados valem zero, e o motivo fica na ficha.
- **Tempo de resposta:** cada requisição tem até 10 segundos para responder; sem resposta, a verificação falha. Se a API deixar de responder (três requisições seguidas sem resposta), a banca reinicia a aplicação uma única vez, pelos comandos do README e sem recriar o banco, e o script retoma o item no pedido que ficou sem resposta: confere pela API se ele foi gravado e, se não foi, reenvia-o igual, mantendo as verificações já feitas no item. Se a API parar de novo, os itens restantes valem zero.
- **Execução única:** o script roda uma vez por candidato. Só é executado de novo em caso de erro nos roteiros.
- **Erro nos roteiros:** se for constatado que uma verificação do script, um passo ou resultado esperado do roteiro da interface, a carga inicial ou o plano de datas contraria o enunciado, ou que o enunciado tem duas regras incompatíveis no ponto verificado, o erro é registrado em ata. Antes da divulgação do resultado, a correção é suspensa, e a nova versão é registrada com tag e hash e reaplicada a **todos** os candidatos, inclusive os já corrigidos; havendo regras incompatíveis, a verificação passa a aceitar as duas leituras. Depois da divulgação, a verificação ou o passo com erro é anulado para todos, o que só mantém ou aumenta as notas. No roteiro da interface, a reavaliação usa o vídeo e o HAR já gravados; se eles não bastarem, o item é executado de novo para todos, a partir do instantâneo da preparação.
- A saída completa do script (requisições, respostas e resultado esperado e obtido de cada verificação) fica com a banca, com o SHA-256 em ata, e não é anexada à ficha; a ficha traz o resultado esperado e o obtido de cada verificação.

### 3.4 Roteiro da interface (F1)

- Executado na tela pela banca, com o mesmo roteiro e os mesmos dados para todos, no Chrome, numa janela de 1366 × 768. A largura de 375 px é usada só no diferencial de responsividade (F5).
- Com o banco recriado, a banca faz pela API a carga inicial prevista no roteiro e executa os itens na ordem da tabela da seção 5. Quando um item precisa de dados que outro item não conseguiu criar, a banca os cria pela API e segue; se a API não conseguir criá-los, os itens que dependem deles valem zero, com o motivo na ficha.
- Cada item é avaliado pelo que a tela faz, conferido no vídeo e no HAR: a tela envia os pedidos previstos no roteiro, mostra o que a API respondeu (valores, ordem, itens filtrados, totais e arquivo) e trata o código de cada resposta. Resposta da API com valor, ordem, filtro, total ou arquivo errados não tira ponto da tela, porque já foi avaliada em B1. O item vale zero quando a tela não envia o pedido previsto, não mostra a resposta recebida ou não trata o código recebido, ou quando a API não devolve a resposta de que o item depende (como a compra aceita do F06).
- Se o frontend chamar a API pelo servidor do Next.js (rewrite, Route Handler ou Server Action), a banca confere os pedidos do navegador ao servidor do Next.js, a tela e, no que não aparecer no HAR, o código.
- O roteiro congelado descreve os passos e o resultado esperado de cada item. Ele só verifica o que o enunciado define: nos pontos deixados à decisão do candidato (como a forma da confirmação ou o lugar de um aviso na tela), qualquer escolha coerente é aceita, e nenhum passo depende dela.
- **Tempo de resposta:** cada ação na tela tem até 10 segundos para mostrar o resultado; sem isso, o item vale zero. Se a aplicação deixar de responder, a banca a reinicia uma única vez, pelos comandos do README e sem recriar o banco, e retoma o item no passo interrompido, conferindo pela API o que já foi gravado; se ela parar de novo, os itens restantes valem zero.
- Botões e textos são reconhecidos pelo sentido, não pela grafia exata (por exemplo, “Excluir” ou “Remover”).
- A execução é gravada em vídeo, e o registro de rede do navegador (arquivo HAR) é salvo; os dois são anexados à ficha. Todo item que valer zero é revisto pelo vídeo e pelo HAR antes de a nota ser fechada.
- O mockup é referência de fluxo e de disposição das telas; a fidelidade visual a ele não conta ponto.

### 3.5 Critérios de leitura (B2 a B5 e F2 a F5)

- Cada critério de B2 a B4 e de F2 a F4 tem três níveis: **atende** (pontuação integral), **atende em parte** (metade) ou **não atende** (zero), com os limites numéricos das tabelas das seções 4 e 5. Quando a situação se enquadra em mais de um nível, vale o mais baixo. Os diferenciais (B5 e F5) valem a pontuação cheia ou zero, como no item **Diferenciais**, abaixo.
- **Um avaliador por projeto:** cada projeto é corrigido por um único avaliador, que preenche a ficha de avaliação e a entrega ao RH. O RH distribui os projetos entre os avaliadores em rodízio, na ordem de recebimento, e registra a distribuição na ata; havendo impedimento (seção 3.7), o projeto passa ao avaliador seguinte do rodízio.
- **Verificações com a aplicação no ar:** F3 e os diferenciais que dependem da aplicação no ar são executados uma vez, na mesma sessão da máquina virtual, depois do roteiro da interface, por um avaliador que segue roteiro fixo, com gravação de tela e HAR: começando com o banco recriado, com a rede desacelerada no perfil registrado na ata e com a navegação feita pela própria interface, sem recarregar a página. O avaliador atribui as notas a partir dessa gravação. O diferencial de Docker é verificado na mesma máquina virtual, com os demais processos parados, em até 30 minutos.
- **Sem dupla penalização:** um defeito que, sozinho, zerou um item do F1 não é contado de novo em F2 ou F3.
- **Ordem e calibração:** a ordem de correção dos projetos é a ordem de recebimento do e-mail de entrega que vale (o último recebido no prazo), registrada na lista de entregas do RH. Antes de começar, os avaliadores corrigem juntos dois projetos fictícios, preparados pela banca, para alinhar a leitura das rubricas.
- **Diferenciais (B5 e F5):** cada diferencial é verificado pelo procedimento das seções 4 e 5 e vale a pontuação cheia ou zero.
- **Item do README ausente ou incorreto (B4 e F4):** ausente é o item sem trecho próprio. Incorreto é o que não corresponde ao repositório (comando que falha como escrito, variável de ambiente usada pelo código e não listada, ou biblioteca listada que não está nas dependências) ou que não traz o que o enunciado pede nele: versões (item 1); origem da API, URL do frontend e arquivos de trava versionados (item 3); motivo de cada biblioteca além da stack obrigatória (item 5); ferramentas, onde, como e por quê e o que foi aceito, alterado ou descartado, ou “Não utilizei” (item 8). Os itens 7 e 8 podem ser um trecho único para o repositório e, se ausentes ou incorretos, contam só em B4. No F4, o item 4 está correto se informar que o frontend não usa variáveis de ambiente, quando for o caso. O item 2 (criação e recriação do banco) é avaliado só em B3 (Criação reprodutível), e não em B4.
- Cada pontuação vem com uma justificativa curta na ficha, apontando os arquivos, trechos ou telas avaliados.

### 3.6 Resultado

- O candidato recebe a nota e a ficha de avaliação, com o resultado esperado e o obtido, a evidência (anexada ou indicada) e a justificativa de cada item e critério.
- **Recurso:** segue o prazo e a forma do regulamento. Para fundamentá-lo, o candidato pode pedir ao RH as evidências que ficam com a banca (o vídeo da preparação e a saída completa do script do B1), e o RH as envia dentro do prazo do recurso. A decisão de cada recurso é registrada em ata, com a justificativa.

### 3.7 Controles da banca

- **Versão oficial:** o enunciado, este barema, o glossário e o exemplo de ficha de avaliação são registrados com uma tag no repositório (por exemplo, `v1.0`), e o hash do commit fica na ata. O mockup é o do link do enunciado, no Figma, na versão v1.0 (id 2409865283741817885 no histórico de versões do arquivo), registrada antes do envio; a coordenação exporta um PDF com todas as telas dessa versão e registra o SHA-256 dele na ata. O mockup não muda depois do envio. Mudança depois do envio só por errata enviada a todos ao mesmo tempo.
- **Roteiros congelados:** o script do roteiro da API, o roteiro da interface, a carga inicial e o plano de datas ficam num repositório restrito à banca e são registrados com tag e hash antes do fim do prazo de entrega. Antes do fim do prazo, a coordenação envia ao RH e ao jurídico, por e-mail institucional, o hash da tag dos roteiros e a configuração da ferramenta de similaridade, e esse e-mail é anexado à ata. Os roteiros não mudam durante a correção, salvo erro nos roteiros (seção 3.3). Eles não são divulgados; a ficha traz o resultado esperado e o obtido de cada verificação, e, no recurso, o candidato pode pedir só a saída do script da própria correção (seção 3.6).
- **Ensaio dos roteiros:** antes do envio do enunciado, a banca executa o script do roteiro da API e o roteiro da interface contra uma implementação de referência, feita por ela a partir do enunciado, com o banco recriado e na imagem de máquina virtual da correção (seção 3.2). Regra incompatível ou exemplo errado no enunciado é corrigido antes do envio (depois dele, só por errata); verificação que contrarie o enunciado é corrigida no script ou no roteiro, que são ensaiados de novo antes de serem congelados. A saída do script e o vídeo do ensaio ficam na ata, com o SHA-256 de cada um, e a implementação fica no repositório restrito à banca, com os roteiros. Os dois projetos fictícios da calibração (seção 3.5) partem dela.
- **Identificação reduzida:** os e-mails de entrega chegam ao coordenador e ao RH. O RH atribui um código a cada candidato e entrega aos avaliadores só o código, o link do repositório e o hash, e o coordenador não repassa nome nem e-mail aos avaliadores. Nome e e-mail ficam com o RH e com o coordenador até todas as notas estarem fechadas. Os avaliadores não abrem o perfil do usuário na plataforma nem pesquisam o candidato; o histórico de envios (B4 e F4) é salvo pela coordenação junto com a cópia. Como o link pode revelar o usuário da plataforma e o coordenador conhece os nomes, a correção não é totalmente cega; por isso valem também as regras de impedimento.
- **Impedimento:** antes do envio do enunciado, quem elabora o enunciado, os roteiros e as respostas às dúvidas assina, com a lista de candidatos convidados, declaração de que não está, em relação a nenhum deles, em nenhuma destas situações: interesse direto ou indireto no resultado; parentesco, inclusive por afinidade, até o terceiro grau; amizade íntima ou inimizade notória; litígio judicial ou administrativo; relação profissional ou acadêmica direta nos últimos 3 anos (subordinação, sociedade, orientação, docência em turma do candidato ou trabalho na mesma equipe). Cada avaliador assina a mesma declaração antes da correção. Havendo impedimento, o RH, que conhece a correspondência entre nomes e códigos, afasta o avaliador do projeto desse candidato. A declaração é renovada depois da identificação; se só então surgir impedimento, as notas dadas pelo avaliador a esse candidato são refeitas por outro avaliador. Com o resultado, os candidatos recebem os nomes dos membros da banca.
- **Integridade das evidências:** o SHA-256 de cada evidência (cópia do repositório, histórico de envios, saída do script, vídeos, arquivos HAR e fichas) é registrado em ata.
- **Guarda das evidências:** evidências, fichas e atas são guardadas pelo prazo de guarda documental do SENAI. A cópia dos repositórios fica com acesso restrito à banca e ao RH.
- **Inteligência artificial na banca:** os avaliadores não usam IA para atribuir notas nem para redigir justificativas e não enviam código, dados ou evidências dos candidatos a serviços externos. A leitura do código é feita em editor com os assistentes de IA desligados. Ferramentas automatizadas só são usadas como previsto neste barema (script do roteiro e detecção de similaridade executada localmente).
- **Ata de correção:** registra datas, avaliadores, versões do script e do roteiro, ambiente (sistema, ferramentas e navegador), ocorrências e notas, e é assinada pela banca.

## 4. Backend (até 5,0)

### B1. Roteiro da API (30 pontos)

| Item | O que é verificado | Regras | Pontos |
| --- | --- | --- | --- |
| **Etapa 1: Jogadores** | | | **9** |
| B01 | Validação do cadastro: corpo que não é objeto, tipos, nomes (espaços e texto vazio), valores de lista, campos obrigatórios ausentes ou nulos, campos fora do snake\_case e limites de cada campo, inclusive as regras que cruzam campos (idade e agilidade, soma dos atributos e potencial) | V1 a V6; Limites de cada campo | 1,5 |
| B02 | Códigos de erro e convenções: JSON inválido (400), caminho e recurso inexistentes (404, inclusive id fora do formato na URL) e regra de negócio (409), sempre com `message` e sem gravar nada; `Content-Type` JSON nas respostas; listas vazias com `200` | V1; V8; V9; Convenções da API | 1 |
| B03 | Campos controlados pelo sistema ignorados, inclusive o valor base enviado no corpo; `201` com `Location`; consulta por id; valor base e indicadores que não mudam no `PUT` | V7; RN08; Convenções da API | 1 |
| B04 | Edição e alteração de condição: validação do corpo do `PUT` e do `PATCH`; idade que não pode diminuir no `PUT`; alteração de condição, inclusive de `DOENTE` direto para `APTO` (409) | V1 a V6; RN08; Limites de cada campo | 1 |
| B05 | Valor de mercado por condição, agilidade e idade, com teto de desconto, piso e arredondamento | RN02 a RN05 | 2 |
| B06 | Indicadores, overall calculado pelos pesos da posição e valor base calculado no cadastro (faixas progressivas do overall, jovem promessa, piso e arredondamento) | RN06 | 1 |
| B07 | Listagem: busca sem diferenciar acentos, filtros combinados (posição, condição, `free=true`, idade e valor de mercado), ordenação (inclusive com dois critérios e desempate), paginação com `meta` e parâmetros inválidos ou contraditórios | RN07; Filtros e query params | 1 |
| B08 | Exclusão lógica de jogador livre: `204` sem corpo, jogador excluído inexistente (404) na consulta, na edição, na alteração de condição e na nova exclusão, e fora de `GET /players` | RN09; V8 | 0,5 |
| **Etapa 2: Clubes** | | | **1,5** |
| B09 | Clubes: `201` com `Location`, caixa inicial de 300,00, formato e unicidade do nome, sigla, limite de 20 clubes e `GET /clubs` ordenado pelo nome | RN10; RN11; Limites de cada campo | 1,5 |
| **Etapa 3: Compra** | | | **5** |
| B10 | Compra: preço pelo valor de mercado, taxa, limite de 50% do caixa sem arredondar, contrato `ATIVO`, transação `COMPRA` e jogador no elenco | RN12; RN13 | 1,5 |
| B11 | Compra recusada: jogador com clube, jogador excluído (404), limite de 12 jogadores no elenco, `club_id` inválido (400) e clube inexistente (404) | RN09; RN12; RN14; V8; Limites de cada campo | 1 |
| B12 | Fim da fidelidade: formato com `-03:00`, outro formato recusado (400), data futura e até 1.095 dias | RN01; Limites de cada campo | 1 |
| B13 | Sequência de compras de jogadores com idades e condições diferentes, conferida pelas respostas e por `GET /clubs/{id}`: valores e caixa de cada compra, elenco na ordem, contrato de cada jogador (fim da fidelidade, dias restantes e % de multa), valor do elenco e patrimônio | RN02 a RN05; RN11; RN13; RN15 | 1,5 |
| **Etapa 4: Venda** | | | **5** |
| B14 | Multa por fidelidade: dias restantes arredondados para cima, faixas de percentual, teto de 10,00 e contrato `RESCINDIDO` ou `ENCERRADO` | RN15 | 2 |
| B15 | Venda: lucro, comissão progressiva (inclusive com prejuízo), crédito no caixa, jogador de volta à lista de livres e transação `VENDA` | RN16 | 2 |
| B16 | Venda recusada (jogador livre e jogador excluído) e recompra: o clube que vendeu o jogador não pode comprá-lo de novo, mas outro clube pode | RN12; RN16; V8 | 1 |
| **Etapa 5: Clubes com elenco** | | | **1** |
| B17 | `GET /clubs` ordenado pelo patrimônio, com desempate, e `sort` inválido (400); `GET /players` com `club_id` e com `free=false`; exclusão de jogador com clube (409); mudança de posição de jogador com clube (409) | RN07; RN09; RN11; Filtros e query params; Limites de cada campo | 1 |
| **Etapa 6: Histórico e exportação** | | | **4** |
| B18 | Histórico: ordem, nome e valores do momento (mesmo depois de editar o jogador), transações de jogador excluído mantidas, conciliação do caixa, filtros por tipo e por jogador, `summary` respeitando os filtros e erros dos filtros, inclusive `player_id` de jogador excluído (404) | RN09; RN17; Filtros e query params | 2 |
| B19 | Exportação CSV: UTF-8 sem BOM, fim de linha LF, linha de cabeçalho, linhas na ordem do histórico com os valores no formato da regra, nome com `;` ou aspas, filtros e erros em JSON | RN18 | 2 |
| **Etapa 7: Liga** | | | **4,5** |
| B20 | Escalação: formação aceita e 5 titulares, com 1 GOL e os jogadores de linha nos setores da formação; `formation` ou `player_ids` fora do formato (400); clube ou jogador inexistente (404); jogador fora do elenco do clube (de outro clube ou livre), jogador `DOENTE` ou posições que não fecham a formação (409), sem gravar nada; escalação substituída por inteiro, sem mudar o caixa; titular que sai da escalação ao ser vendido ou ao passar a `DOENTE`; `GET /clubs/{id}/lineup` com `formation` e `complete`, na ordem do elenco | RN19; V8; V9; Limites de cada campo | 1,5 |
| B21 | Partida: `201` com `Location`; placar pelos 6 duelos, na ordem da regra, com atacantes e defensores escolhidos pela ordem do elenco e o atributo de ataque pela posição do atacante; gol só quando o ataque é maior que a defesa (duelo empatado não é gol); titular `MAL_CONDICIONADO` com 15% a menos em cada atributo, com o arredondamento da regra; `result` pelos gols de cada clube (`MANDANTE`, `VISITANTE` ou `EMPATE`); partida que não muda o caixa, a escalação nem os jogadores; mandante igual ao visitante (400), clube inexistente (404) e clube sem escalação completa (409); formações e duelos gravados com os nomes, as posições, as condições e os valores do momento | RN20; V8; V9 | 2 |
| B22 | Histórico de partidas e classificação: `GET /matches` da mais recente para a mais antiga, filtro `club_id` e seus erros; `GET /matches/{id}` com os 6 duelos; `GET /standings` com todos os clubes, pontos e desempates (saldo de gols, gols marcados e nome) | RN21; Filtros e query params | 1 |
| **Total** | | | **30** |

### B2. Qualidade do código do backend (10 pontos)

| Critério | Pontos | Atende | Atende em parte (metade) | Não atende (zero) |
| --- | --- | --- | --- | --- |
| Camadas | 2 | Nenhuma ocorrência | 1 ou 2 ocorrências | 3 ou mais ocorrências |
| Regras de negócio | 2 | Cada um dos 6 cálculos (valor de mercado, overall, taxa, multa, comissão e placar da partida) implementado em um único lugar | 1 cálculo duplicado | 2 ou mais cálculos duplicados |
| Validação e erros | 2 | Todos os endpoints validam a entrada por um mecanismo declarado, as recusas passam por um tratamento central de erros e nenhuma resposta traz stack trace | 1 ou 2 endpoints fora disso | 3 ou mais endpoints fora disso, ou stack trace exposto |
| Consistência dos dados | 2 | Compra, venda, partida (com os 6 duelos), escalação e alteração de condição que tira um titular, cada uma numa transação do banco | De uma a quatro dessas operações em transação | Nenhuma delas em transação |
| Segurança e configuração | 1 | As 4 práticas: consultas parametrizadas ou ORM, sem concatenar valores recebidos em SQL; segredos lidos de variáveis de ambiente; CORS restrito à origem do frontend; nenhuma credencial real no repositório | 3 das 4 práticas | 2 ou menos |
| Código morto e padrão | 1 | Nenhum arquivo do backend com código comentado, código sem uso ou nomes fora do padrão | 1 a 5 arquivos | Mais de 5 arquivos |

Como contar:

- **Ocorrência (camadas):** cada rota ou método de controlador que calcula regra de negócio (RN02 a RN06, RN11, RN13, RN15 a RN17, RN20 e RN21) ou acessa o banco diretamente (SQL ou ORM), em vez de chamar a camada de serviço ou de dados. Não contam a validação declarativa de entrada (DTO, schema ou serializer), o `queryset` e o `serializer_class` declarados em views genéricas do Django REST Framework, nem o `get_queryset` que só aplica os filtros, a ordenação e a paginação recebidos.
- **Cálculo duplicado:** a mesma fórmula implementada em dois ou mais lugares do backend. Não contam os testes automatizados nem a fórmula do valor de mercado escrita em SQL para filtrar e ordenar listagens (RN07 e ordenação de clubes pelo patrimônio, na RN11). A multa inclui os dias restantes e o percentual (RN15), usados também na consulta do clube.
- **Endpoint:** cada método e rota das tabelas de “2. Endpoints” do enunciado que recebe corpo, query params ou id na URL.
- **Mecanismo declarado:** DTO, schema ou serializer com validação, pipe, middleware, dependência, conversor ou expressão regular de rota, ou função de validação reutilizada chamada antes da lógica do endpoint; `if` no próprio método do controlador não conta.
- **Operação numa transação:** todas as gravações da operação ficam numa única transação do banco: na compra, o caixa, o elenco, o contrato e a transação `COMPRA`; na venda, o caixa, o jogador livre, o contrato, a transação `VENDA` e a saída da escalação; na partida, a partida e os 6 duelos; na escalação, a formação e os 5 titulares; na alteração de condição para `DOENTE`, a condição e a saída da escalação.
- **CORS restrito:** a API libera só a origem do frontend, lida de variável de ambiente ou de arquivo de configuração; `*`, origem refletida sem conferência ou API sem CORS, mesmo com proxy no frontend, não atende.
- **Segredo:** senha do banco e chave usada pela aplicação (como a `SECRET_KEY` do Django). Um segredo escrito no código conta só na prática dos segredos, e não como credencial real.
- **Credencial real:** senha, token ou chave de serviço. Valores de exemplo do `.env.example` e senhas de banco local usadas só no ambiente de desenvolvimento (como no Docker Compose) não contam.
- **Código morto e padrão:** código comentado, código sem uso e nomes fora do padrão contam como no F2, no código da pasta `backend/`. Além dos nomes que o F2 exclui, também não contam as tabelas e colunas do banco definidas pelo enunciado (“3. Estrutura de tabelas”) nem os identificadores que só as espelham no mapeamento do ORM.

### B3. Banco de dados (6 pontos)

| Critério | Atende (2) | Atende em parte (1) | Não atende (0) |
| --- | --- | --- | --- |
| Criação reprodutível | Os comandos do README criam e recriam o banco do zero, por migrations ou script versionado | Criam, mas a recriação não está documentada ou falha | O banco não é criado pelos comandos do README |
| Estrutura | Nenhum desvio em relação a “3. Estrutura de tabelas” | 1 ou 2 desvios | 3 ou mais desvios, ou tabela obrigatória faltando |
| Restrições | Unicidade garantida no banco para o nome do clube (conforme a RN10), a sigla e o jogador em uma só escalação (`escalacoes.jogador_id`), e nenhuma coluna de valor calculado | 1 falha | 2 ou mais falhas |

Como contar:

- **Script versionado:** inclui a criação das tabelas pelo ORM ao iniciar a aplicação, a partir do código versionado.
- **Desvio:** cada tabela, coluna, chave primária ou chave estrangeira obrigatória ausente ou com outro nome, e cada coluna de moeda fora de DECIMAL, NUMERIC ou inteiro em centavos. Na `escalacoes`, a chave primária é composta por `clube_id` e `jogador_id`; chave primária em outras colunas conta como desvio. Colunas, tabelas e índices adicionais não contam.
- **Falha:** cada unicidade ausente no banco ou com comparação diferente da exigida (nome do clube conforme a RN10; jogador em uma só escalação), e cada coluna que grava valor calculado (valor de mercado, overall, valor do elenco, patrimônio, dias restantes, percentual de multa, pontos ou posição na classificação). Unicidade de tabela ou coluna ausente, já contada como desvio, não conta como falha.
- **Conferência das unicidades:** no banco recriado depois dos roteiros, com inserções diretas definidas no roteiro congelado: “Águias FC” e “águias fc” são recusados como repetidos; “Águias FC” e “Aguias FC” são aceitos; duas siglas iguais são recusadas; o mesmo jogador em duas escalações é recusado. Cada inserção parte de uma linha criada antes pela API e troca só o id, o valor conferido e as outras colunas únicas, que recebem valores novos; a coluna normalizada do nome preenchida pela aplicação, se houver, recebe o valor que o código da aplicação calcularia para o nome inserido. Se a API não criar a linha, as colunas recebem valores válidos definidos no roteiro.

### B4. README e histórico do Git do backend (2 pontos)

| Critério | Atende (1) | Atende em parte (0,5) | Não atende (0) |
| --- | --- | --- | --- |
| README do backend | Os itens 1 e 3 a 8 de “📘 Requisitos do README.md” presentes e corretos na parte do backend | 1 ou 2 itens ausentes ou incorretos | 3 ou mais itens ausentes ou incorretos, ou sem como executar o backend |
| Histórico do Git | Pelo menos 10 commits que alteram a pasta `backend/`, enviados (push) em pelo menos 3 dias diferentes, com no máximo metade das mensagens genéricas | De 3 a 9 commits, ou envios em menos de 3 dias, ou mais da metade das mensagens genéricas | Até 2 commits |

Como contar (vale também para F4):

- **Commits:** os do histórico do commit informado (ele e os anteriores) que alteram pelo menos um arquivo da pasta. Merges sem alteração própria não contam.
- **Dias de envio:** dias diferentes, no horário de Brasília, em que houve envio (push) de commits contados, até o fim do prazo, segundo o histórico de envios salvo junto com a cópia (seção 3.1). As datas dos commits não são usadas, porque podem ser alteradas por quem faz o commit.
- **Mensagem genérica:** a que, sem considerar maiúsculas, acentos, pontuação e números, é vazia ou formada só por palavras desta lista: ajuste, ajustes, alteração, alterações, atualização, atualizações, change, changes, commit, correção, correções, final, fix, fixes, misc, teste, testes, test, tests, update, updates, versão, wip.

### B5. Diferenciais técnicos do backend (2 pontos)

Cada diferencial vale **0,5 ponto**, até o máximo de **2 pontos**, quando o README explica como executá-lo e a verificação abaixo passa:

- **Testes automatizados:** o comando de testes do README termina sozinho, sem modo de observação, em até 10 minutos e sem falhas, e pelo menos um teste confere o valor de mercado calculado (RN02 a RN05).
- **Docker e Docker Compose:** um único comando do README sobe interface, API e banco, e a lista de jogadores abre na URL do frontend.
- **Documentação interativa da API (Swagger ou OpenAPI):** a URL informada no README abre a documentação, com todos os endpoints das tabelas de “2. Endpoints”.
- **Registro de logs:** depois de uma requisição, a saída da aplicação mostra uma única linha com data e hora legíveis, método, caminho e status dessa requisição, gerada por biblioteca de log declarada nas dependências ou fornecida pelo framework ou pela biblioteca padrão; `print` e `console.log` não contam.
- **Lint e formatação:** os comandos de lint e de verificação da formatação do backend, informados no README, terminam sem erros, e o de formatação só verifica, sem alterar arquivos.

## 5. Frontend (até 5,0)

### F1. Roteiro da interface (30 pontos)

| Item | O que é verificado pela tela | Pontos |
| --- | --- | --- |
| **Etapa 1: Jogadores** | | **7** |
| F01 | Tabela de jogadores com nome, posição, overall, agilidade, idade, condição, valor base, valor de mercado e clube (“Livre” quando não houver); paginação de 10 por página, com navegação entre páginas e total de jogadores encontrados | 2 |
| F02 | Busca por nome; filtros por posição, condição, só livres, faixa de idade e faixa de valor de mercado, combináveis; ordenação por nome, por valor de mercado e por idade (estas duas nos dois sentidos) e por posição; com só livres e clube juntos, a tela impede a combinação ou mostra o `message` da API | 2 |
| F03 | Botão Excluir nos jogadores livres, com confirmação, e o jogador sai da lista | 1 |
| F04 | Cadastro com os sete indicadores informados (o valor base e o overall aparecem calculados depois de salvar), edição e alteração de condição | 2 |
| **Etapa 2: Clubes** | | **2** |
| F05 | Clubes: listagem com nome, sigla, caixa, valor do elenco e patrimônio, ordenada por nome, na ordem devolvida pela API, e formulário de criação | 2 |
| **Etapa 3: Compra e venda** | | **8** |
| F06 | Compra a partir da lista de jogadores livres: escolha do clube, fim da fidelidade digitado no horário de Brasília e enviado com `-03:00`, confirmação e resultado com valor, taxa, custo total (valor + taxa), fim da fidelidade e novo caixa; depois da compra, a tabela de jogadores mostra o clube (nome ou sigla), o filtro por clube encontra o jogador e o filtro só livres deixa de mostrá-lo | 3 |
| F07 | Página do clube depois das compras: caixa, valor do elenco, patrimônio e elenco na ordem devolvida pela API, com o valor de mercado de cada jogador e as colunas do contrato (fim da fidelidade, dias restantes e % de multa); lista de clubes ordenada por patrimônio, do maior para o menor, na ordem devolvida pela API, com patrimônios diferentes depois de compras com taxa | 2 |
| F08 | Venda pelo botão Vender, na página do clube, com confirmação, e resultado: valor de compra, valor de venda, dias restantes, multa, lucro, comissão, crédito e novo caixa | 3 |
| **Etapa 4: Histórico** | | **6** |
| F09 | Histórico na página do clube: data e hora, tipo, jogador, valor, taxa ou comissão, multa, lucro e variação do caixa com sinal (“+” e “-”); filtro por um ou mais tipos e por jogador e, se a API recusar o filtro (jogador excluído), o `message` da API | 3 |
| F10 | Totais do `summary` abaixo da tabela, respeitando o filtro | 2 |
| F11 | Botão Exportar CSV, que baixa o arquivo devolvido pela API (RN18), pedido com os filtros aplicados | 1 |
| **Etapa 5: Liga** | | **7** |
| F12 | Escalação, na página do clube: escolha da formação e de um titular para cada vaga dela (1 goleiro e os 4 jogadores de linha), entre os jogadores do elenco, sem `DOENTE`; depois de salvar, a tela mostra a escalação devolvida pela API; com a escalação incompleta, aviso de que o clube não pode jogar | 2 |
| F13 | Partida: escolha do mandante e do visitante e resultado com o placar e os 6 duelos devolvidos pela API (atacante, defensor, atributos, valores e gol), sem recalcular; com um clube sem escalação completa, o `message` da API | 3 |
| F14 | Histórico de partidas (data e hora, mandante, placar e visitante, da mais recente para a mais antiga, com filtro por clube e os duelos ao abrir uma partida) e classificação na ordem devolvida pela API, com jogos, vitórias, empates, derrotas, gols marcados, gols sofridos, saldo e pontos | 2 |
| **Total** | | **30** |

### F2. Qualidade do código do frontend (10 pontos)

| Critério | Atende (2) | Atende em parte (1) | Não atende (0) |
| --- | --- | --- | --- |
| Componentes | Nenhum dos três (tabela, formulário e mensagens) duplicado entre telas | 1 deles duplicado | 2 ou 3 duplicados |
| Acesso à API | Todas as chamadas à API numa camada própria (serviço, cliente ou hooks de dados), sem chamada direta em componentes | 1 ou 2 componentes com chamada direta | 3 ou mais |
| Atualização e regras | Depois de cada uma das 9 ações, a tela mostra os dados atualizados pela API, sem recarregar a página, e nenhuma regra é recalculada na tela | 1 ou 2 ações sem atualização | 3 ou mais ações sem atualização, ou regra recalculada na tela |
| Formulários | Os 7 formulários validam, antes de enviar, os campos obrigatórios e os limites listados abaixo, mostram a mensagem junto ao campo e enviam as datas com `-03:00` | 1 ou 2 formulários fora disso | 3 ou mais |
| Código morto e padrão | Nenhum arquivo do frontend com código comentado, código sem uso ou nomes fora do padrão | 1 a 5 arquivos | Mais de 5 arquivos |

Como contar:

- **Duplicado:** o mesmo trecho de marcação e lógica (cabeçalho e linhas com os estados de carregamento, vazio e erro; campo com rótulo e mensagem de erro; aviso de sucesso e de erro) escrito em duas ou mais telas, em vez de vir de um componente compartilhado, próprio ou de biblioteca. Usar o mesmo componente com colunas ou campos diferentes não é duplicação.
- **Chamada direta:** `fetch`, Axios ou equivalente usado dentro de qualquer componente React, de tela ou não; conta-se cada componente.
- **As 9 ações:** cadastrar, editar e alterar a condição de um jogador; excluir; criar clube; comprar; vender; escalar; jogar partida.
- **Regra recalculada:** valor base, valor de mercado, overall, taxa, multa, comissão, lucro, crédito, valor do elenco, patrimônio, dias restantes, percentual de multa, totais do `summary`, placar, duelos ou classificação calculados na tela em vez de lidos da API. Somar valor e taxa para mostrar o custo total é permitido.
- **Os 7 formulários:** cadastro e edição de jogador, alteração de condição, criação de clube, compra, escalação e nova partida. A validação exigida antes de enviar cobre os campos obrigatórios (na escalação, a formação e um titular em cada uma das 5 vagas; na partida, o mandante e o visitante), o tamanho dos textos (nome do jogador de 3 a 100 caracteres, nome do clube de 3 a 60, sigla com 3 letras) e as faixas de um campo só (agilidade de 1 a 100, idade de 16 a 45, atributos e potencial de 1 a 99). Formato de nomes e da sigla, limites que dependem do momento atual e regras que cruzam campos podem ficar só na API. As regras que dependem do banco ficam na API: a tela envia o pedido e mostra o `message`, salvo nas recusas que o enunciado permite impedir (seção 🖥️ Frontend, “Mensagens e apresentação”).
- **Conferência pelo uso:** Atualização e regras e Formulários são conferidos pelo uso da interface, nas gravações do F1 e do F3, e confirmados pela leitura do código; se o backend ou o frontend não subir, só pela leitura do código.
- **Código sem uso:** arquivo, componente, função ou variável que nenhum outro trecho do projeto usa, constatado por busca de texto no código-fonte.
- **Nomes fora do padrão:** identificadores em mais de um idioma ou fora das convenções da linguagem (como `camelCase` para funções e variáveis e `PascalCase` para componentes). Não contam os nomes definidos pelo enunciado: campos e query params da API em snake\_case, valores de lista (como `APTO`, `MAL_CONDICIONADO` e `COMPRA`) e textos exibidos na tela.

### F3. Usabilidade e feedback (6 pontos)

| Critério | Atende (2) | Atende em parte (1) | Não atende (0) |
| --- | --- | --- | --- |
| Mensagens | As 9 ações mostram mensagem de sucesso e, quando recusadas, o `message` devolvido pela API, e o clique duplo envia um só pedido | 1 ou 2 ações fora disso | 3 ou mais |
| Estados das telas | Carregamento, lista vazia e erro nas 6 telas de lista | Falta em 1 ou 2 telas | Falta em 3 ou mais |
| Apresentação | Valores em moedas com 2 casas e vírgula decimal e datas no horário de Brasília nas 6 telas listadas abaixo | 1 ou 2 telas fora do padrão | 3 ou mais |

Como verificar (na sessão gravada da seção 3.5):

- **Mensagens:** cada uma das 9 ações (F2) é executada uma vez com sucesso e, quando o roteiro prevê, uma vez com recusa da API, sempre de regra que depende dos dados gravados (`409` ou `404`), nunca de validação de formulário (F2). No envio com sucesso, o botão da ação é clicado duas vezes seguidas, e o HAR precisa mostrar um só pedido. Mensagem genérica no lugar do `message` da API conta como fora disso. Nas recusas que o enunciado permite impedir na tela (seção 🖥️ Frontend, “Mensagens e apresentação”), impedir a ação, mostrando o motivo, também atende.
- **Estados das telas:** as 6 telas de lista são jogadores, clubes, elenco do clube, histórico de transações, histórico de partidas e classificação. A lista vazia é vista com o banco recém-recriado e num clube recém-criado; o carregamento, com a rede desacelerada; o erro, com o backend parado.
- **Apresentação:** as 6 telas são lista de jogadores, clubes, página do clube (com o histórico de transações), resultado da compra, resultado da venda e histórico de partidas.

### F4. README e histórico do Git do frontend (2 pontos)

| Critério | Atende (1) | Atende em parte (0,5) | Não atende (0) |
| --- | --- | --- | --- |
| README do frontend | Os itens 1, 3, 4 e 5 de “📘 Requisitos do README.md” presentes e corretos na parte do frontend | 1 ou 2 itens ausentes ou incorretos | 3 ou mais itens ausentes ou incorretos, ou sem como executar o frontend |
| Histórico do Git | Pelo menos 10 commits que alteram a pasta `frontend/`, enviados (push) em pelo menos 3 dias diferentes, com no máximo metade das mensagens genéricas | De 3 a 9 commits, ou envios em menos de 3 dias, ou mais da metade das mensagens genéricas | Até 2 commits |

Commits, dias de envio e mensagens genéricas são contados como em B4. Os itens 7 e 8 contam só em B4 (seção 3.5).

### F5. Diferenciais de interface (2 pontos)

- **Responsividade (1 ponto):** no modo dispositivo do Chrome, com 375 px de largura, a lista de jogadores e a página do clube, com o histórico, não têm rolagem horizontal da página (tabelas podem rolar dentro do próprio quadro), e todas as ações dessas telas continuam acessíveis.
- **Testes no frontend (1 ponto):** o comando de testes do frontend informado no README termina sozinho, sem modo de observação, em até 10 minutos e sem falhas, com pelo menos um teste de componente ou de ponta a ponta.
- **Lint e formatação (0,5 ponto):** os comandos de lint e de verificação da formatação do frontend, informados no README, terminam sem erros, e o de formatação só verifica, sem alterar arquivos.

Os diferenciais somam até 2,5 pontos, limitados ao máximo de 2.

## 6. Exemplo de cálculo da nota

| Parte | Pontos por critério | Pontos | Na nota |
| --- | --- | --- | --- |
| Backend | B1 24 + B2 8 + B3 6 + B4 1,5 + B5 1 | 40,5 | 4,05 |
| Frontend | F1 22 + F2 7 + F3 5 + F4 1 + F5 1 | 36 | 3,60 |
| **Total** | | **76,5** | **7,65** |

Resultado: aprovado, porque a nota final é pelo menos 7,0 e as duas partes têm pelo menos 2,5.
