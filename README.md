### O Evolke
O Evolke é um software desenvolvido para a **gestão da carreiras** de servidores Técnicos-Administrativos em Educação (TAE) e do Magistério Federal (Superior e EBTT), de que tratam as Leis nº 11.091/2005 e 12.772/2012, respectivamente. Seus recursos permitem planejar, executar e controlar concessões e progressões funcionais, lotações; gerar listagens e relatórios diversos; bem como integrar dados oriundos de arquivos e sistemas de terceiros.

### Versão 2.2.0.0 (12/12/2023)
O que há de novo nesta versão?

[SISTEMA]
- Distribuição do sistema alterada para a arquitetura de software de 64 bits.
- Inclusão de atalho para o sistema no menu de contexto do SO Windows.
- Ajuste para suporte a drivers ODBC MySQL de 64 bits, apos ajuste - versão compatível recomendada MySQL ODBC 8.0.32, disponível em https://downloads.mysql.com/archives/get/p/10/file/mysql-connector-odbc-8.0.32-winx64.msi.
- Abrangente remodelagem da infraestrutura de código fonte do software para implementação de suporte a transposições entre diferentes estruturas de carreiras ao longo da vida funcional do vínculo.
- Função "Estrutura Mínima de Carreira" aprimorada e renomeada para "Projeção de Carreira", que realiza a análise de ocorrências e a prioriza sobre o histórico de posicionamentos, exceto quando houver enquadramento/transposição, posicionamento por titulação/capacitação ou decisão administrativa.
- Em Minhas Preferências, inclusão de opções para seleção de monitor de vídeo.

[CADASTRO]
- Cadastro de Pessoas renomeado para Cadastro de Pessoas Físicas.
- Em Cadastro de Pessoas Físicas, ajustes e melhorias de desempenho.
- Em Ações de Desenvolvimento, ajustes de layout e melhoria do mecanismo de pesquisa.

[CARREIRAS]
- Em Histórico de Posicionamentos, inclusão das opções de Notificações Eletrônicas e acesso à Central de Notificações no menu de contexto do grid superior de vínculos.
- Em Progressões Funcionais, realizadas as seguintes inclusões e melhorias:
  - Ajuste de regra que permite realizar progressão que não seja por capacitação em DL de Progressão por Capacitação e, se ocorrer, marcar como posicionamento por titulação/capacitação - recurso especialmente aplicável para o desenvolvimento na estrutura de carreira do Plano Único de Classificação e Retribuição de Cargos e Empregos (PUCRCE);
  - Inclusão de filtros extras em Filtros Dinâmicos.

[FERRAMENTAS]
- Tela Análise de Ocorrências e Projeção de Carreira simplificada, com remoção da distinção entre os tipos de análise individual e em lote, os quais passam a ser tratados como um único tipo.
- Em Central de Notificações, inclusão da tag <REGVINCMULTICONC-MSG>, a ser substituída por informação de vínculos com mais de uma concessão considerando os DLs selecionados para envio.
- Em Integração Sistêmica, ajustes na integração de Ações de Desenvolvimento, em razão do arredondamento de carga horária existente no arquivo importado (Ex.: Curso com carga horária "42:30" informado como "43" no arquivo).

[RELATÓRIOS]
- Em Listagens, em Progressões e Concessões Efetivadas, inclusão do filtro "por vínculo/lotação" no menu de contexto, o qual realiza a pesquisa considerando as unidades de lotação selecionadas em vez dos DL associados à unidade logada pelo usuário.

[OUTROS]
- Em diversas telas do sistema, nos grids em que a função de clique sobre o título das colunas estiver habilitada, inclusão da múltipla seleção de colunas, ao clicar-se sobre seus títulos mantendo-se a tecla Ctrl pressionada, para ordenação dos registros.
- Ajustes e melhorias na tela Pesquisa de Pessoas Físicas.
- Ajustes e melhorias nas configurações de seleção de monitor de vídeo.
- Melhorias pontuais de estabilidade e prevenção de bugs.
