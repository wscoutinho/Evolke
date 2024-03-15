### O Evolke

O Evolke é um software desenvolvido para a **gestão da carreiras** de servidores Técnicos-Administrativos em Educação (TAE) e do Magistério Federal (Superior e EBTT), de que tratam as Leis nº 11.091/2005 e 12.772/2012, respectivamente. Seus recursos permitem planejar, executar e controlar concessões e progressões funcionais, lotações; gerar listagens e relatórios diversos; bem como integrar dados oriundos de arquivos e sistemas de terceiros.

Pré-requisitos (primeira instalação):

- [Visual C++ Redistributable](https://github.com/wscoutinho/Evolke/raw/main/assets/VC_redist.x86.exe)
- [Conector ODBC MySQL 8.3](https://github.com/wscoutinho/Evolke/raw/main/assets/mysql_8.3.0.msi)

Download Evolke:

- [Versão atual (Latest)](https://github.com/wscoutinho/Evolke/releases)

---

O que há de novo? Confirma as notas de versão:

### Versão 2.2.3.0 (Atual)

[SISTEMA]

- Correção do modo de teste de conexão ICMPIndy (RAW Socket), que, ainda que houvesse conectividade com o servidor, indicava ausência de conectividade e impedia a plena utilização do sistema.
- Ajuste nas operações de backup e restore de banco de dados em razão da utilização da versão 8.3 do conector ODBC MySQL.

[CADASTRO]

- Em Cadastro de Unidades Organizacionais, realizadas as seguintes inclusões e melhorias:
  - Inclusão do cadastro de Contatos e Dirigentes, possibilitando o registro atual e histórico de titulares e substitutos e respectivos contatos de e-mail e telefone;
  - Inclusão, no menu de contexto, de opções de acesso ao cadastro e ao relatório de Contatos e Dirigentes.

[CARREIRAS]

- Em Progressões Funcionais, correção na função Alterar DL Vinculado em Lote.

[RELATÓRIOS]

- Em Relatórios Gerais, inclusão do relatório Contatos e Dirigentes das Unidadades Organizacionais.

[OUTROS]

- Melhorias pontuais de estabilidade e prevenção de bugs.

---

### Versão 2.2.2.0 (08/02/2024)

[SISTEMA]

- Distribuição do novo driver "MySQL Connector ODBC 8.3 (64-bit)" e ajustes de compatibillidade necessários.
- Inclusão de novo modo de teste de conexão "DBCheck (Flag Select)" mais apurado em relação aos preexistentes e compatível com o novo driver conector MySQL ao restabelecer, via aplicação, a conexão com o banco de dados.

[CADASTRO]

- Em Cadatro de Diplomas Legais, inclusão dos assuntos Enquadramento/Transposição para carreiras e para concessões.

[CARREIRAS]

- Em Progressões e Concessões Funcionais, inclusão de indicador de pendência na progressão ou concessão.
- Em Progressões Funcionais, inclusão do suporte a Diplomas Legais de enquadramento/transposição de carreira, com registro no histórico de posicionamentos e, se cabível, atualização do posicionamento vigente.

[RELATÓRIOS]

- Em Relatórios Gerais, no Dossiê do Vínculo, ajuste para exibição da denominação correta de um posicionamento específico em função da titulação, quando houver, p. ex., para a classe A da Carreira do Magistério Superior, conforme Lei nº 12.772/2012.

[OUTROS]

- Correções pontuais de bugs provenientes da nova implementação do suporte a múltiplas carreiras.
- Melhorias pontuais de estabilidade e prevenção de bugs.

---

### Versão 2.2.1.0 (09/01/2024)

[CARREIRAS]

- Em Histórico de Posicionamentos e Progressões Funcionais, inclusão dos itens "Outras" no filtro Categoria e "Avaliação" no filtro Carreira TAE, agora renomeado para Tipo, que permitem expandir a consulta a outras designações de carreira além de TAE e DOCENTE e outros tipos além de Mérito (M), Capacitação (C) e Único (U).
- Em Progressões Funcionais, inclusão de filtro extra em Filtros Dinâmicos para obter todos os vínculos que podem acelerar ou progregir por titulação/capacitação, independente da existência de progressão funcional pendente.

[FERRAMENTAS]

- Em Análise de Ocorrências e Projeção de Carreira, realizadas as seguintes inclusões e melhorias:
  - Inclusão de opções de análise, agrupando opções existentes e acrescentando a opção "desconsiderar decisão administrativa", o que permite realizar projeções outras que não considerem posicionamentos cadastrados como decisão administativa;
  - Ajuste na rotina de projeção para considerar a titulação do vínculo na data de vigência de cada posicionamento cadastrado, e não a titulação atual, o que permite melhor adequação da projeção.

[OUTROS]

- Correções pontuais de bugs provenientes da nova implementação do suporte a múltiplas carreiras.
- Correção da rotina de atualização diária automática da vigência prevista para vínculos que possuem vigente ocorrência que suspende a contagem do interstício atual para a próxima progressão.
- Melhorias pontuais de estabilidade e prevenção de bugs.

---

### Versão 2.2.0.0 (12/12/2023)

[SISTEMA]

- Distribuição do sistema alterada para a arquitetura de software de 64 bits.
- Inclusão de atalho para o sistema no menu de contexto do SO Windows.
- Ajuste para suporte a drivers ODBC MySQL de 64 bits, apos ajuste - Versão compatível recomendada MySQL ODBC 8.0.32, disponível em https://downloads.mysql.com/archives/get/p/10/file/mysql-connector-odbc-8.0.32-winx64.msi.
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

---

### Versão 2.1.0.8 (23/08/2023)

[TELA PRINCIPAL]

- No painel de DLs Abertos, inclusão da opção "Selecionar Tudo" no menu de contexto.
- No painel de menus, remoção da opção Integração Sistêmica, que agora deve ser acessada somente pelo menu de contexto do sistema ou pelo menu lateral.

[CADASTRO]

- Em Ocorrências Funcionais, melhoria de desempenho ao editar ou incluir uma ocorrência.
- Inclusão da tela Ações de Desenvolvimento.
- Em Instituições Externas, melhorias de layout e desempenho.

[CARREIRAS]

- Em Progressões Funcionais, inclusão do carregamento de ocorrências recentes ao carregar-se um DL.
- Em Progressões e Concessões Funcionais, realizadas as seguintes inclusões e melhorias:
  - Nos menus de contexto, inclusão de opção de consulta de Ações de Desenvolvimento;
  - Verificação entre o vínculo a ser adicionado a um DL e o tipo padrão de carreira a que se relaciona o DL, com mensagem de alerta nos casos de inclusão potencialmente incompatível.
- Preparação para futura inclusão da tela Desenvolvimento de Pessoas.
- Análise de Ocorrências funcionais renomeada para Análise e Projeção de Carreira e movida para o módulo Ferramentas.

[FERRAMENTAS]

- Análise e Projeção de Carreira movida do módulo Carreiras.
- Em Integração Sistêmica, inclusão da importação de Instituições Externas e de Ações de Desenvolvimento.

[OUTROS]

- Ajustes e melhorias na Pesquisa de Instituição Externa.
- Melhorias pontuais de estabilidade e prevenção de bugs.

---

### Versão 2.1.0.7 (21/06/2023)

[SISTEMA]

- Tela "Preferências do Usuário" renomeada para "Minhas Preferências".

[CARREIRAS]

- Em Concessões Funcionais, ajuste na titulação equivalente ao RSC a ser mostrado na minuta de portaria MS Word.

[FERRAMENTAS]

- Em Integração Sistêmica, realizadas as seguintes inclusões e melhorias:
  - Correção na importação de licenças quando selecionada a opção de inclusão de vínculos inativos, de maneira a evitar o registro de ocorrências em duplicidade;
  - Inclusão da importação padrão de registros de Licença para Capacitação.
- Em Central de Notificações, realizadas as seguintes inclusões e melhorias:
  - Ajustes na rotina de envio de Mala Direta;
  - Novas TAGs adicionadas para configuração de Mala Direta;
  - Inclusão da origem de dados Planilha Eletrônica na configuração de Mala Direta.

[RELATÓRIOS]

- Em Listagens, inclusão da coluna Progride na listagem Licenças para Tratamento de Saúde (Controle), que permite identificar melhor os vínculos que ainda possuem progressão funcional a realizar.

[OUTROS]

- Simplificação do aviso visual de ausência de conectividade com o servidor nas telas do sistema.
- Correções necessárias para compatibilidade com o SO Windows 7 e na operação de logoff.
- Melhorias pontuais de estabilidade e prevenção de bugs.

---

### Versão 2.1.0.6 (02/05/2023)

[SISTEMA]

- Em Configurações de Sistema, inclusão das seguintes novas configurações:
  - Definição de valor padrão (Sim/Não) para o campo Pendência da inclusão de nova concessão na tela de Concessões Funcionais, para cada tipo de concessão;
  - Retribuição por Titulação com status pendente verifica e atualiza previsão de progressão (Padrão: desativado).

[TELA PRINCIPAL]

- Na barra de status, inclusão de indicador visual de conectividade nula ou limitada quando o desempenho corrente da conexão com o servidor, isto é, dos últimos testes de conexão, encontra-se abaixo do percentual mínimo recomendado (90%).

[CARREIRAS]

- Em Histórico de Posicionamentos, incremento na possibilidade de expansão do grid inferior, para melhor visualização dos registros sem que seja necessário alterar a opção de visualização da tela.
- Em Concessões Funcionais, realizadas as seguintes inclusões e melhorias:
  - Incremento na possibilidade de expansão do grid inferior, para melhor visualização dos registros sem que seja necessário alterar a opção de visualização da tela;
  - Melhoria visual do grid superior com inclusão do campo Status;
  - Melhoria no campo Pendência da concessão em inclusão, com valor padrão previamente configurado no sistema.
- Em Progressões Funcionais, realizadas as seguintes inclusões e melhorias:
  - Incremento na possibilidade de expansão do grid inferior, para melhor visualização dos registros sem que seja necessário alterar a opção de visualização da tela;
  - Melhoria visual do grid superior com inclusão do campo Status e destaque do campo Previsão.

[FERRAMENTAS]

- Em Integração Sistêmica, ajuste na importação de vínculos para detecção de vínculos inativos no sistema, porém reativados na fonte de dados (p. ex.: em razão de reversão de aposentadoria).
- Em Central de Notificações, realizadas as seguintes inclusões e melhorias:
  - Inclusão do recurso Mala Direta, a partir de TAGs próprias a serem automaticamente substituídas e envio individual de notificação, com os respectivos dados de cada destinatário;
  - Ao criar-se um modelo-padrão de e-mail exclusivo para mala direta, pode-se incluir, no Assunto, o termo "[Mala Direta]", sem aspas, o qual será automaticamente removido quando da formatação e envio do e-mail;
  - Ao criar-se um novo modelo-padrão, é possível fazê-lo como cópia de um modelo existente; para tanto, deve-se editar o modelo existente de referência e, através do menu de contexto, clicar na opção "Duplicar Modelo";
  - Melhoria no envio de e-mail, com destaque para o nome dos destinatários no e-mail de confirmação enviado ao remetente.

[RELATÓRIOS]

- Em Listagens, realizadas as seguintes inclusões e melhorias:
  - Inclusão do campo Status na listagem Progressões e Concessões Funcionais com Pendência;
  - Inclusão, no menu de contexto, da opção Listagem, para retorno ao grid principal com o rol das listagens disponíveis.

[OUTROS]

- Melhorias pontuais de estabilidade e prevenção de bugs.
- Nas telas do sistema, inclusão de recurso que permite sair de um Grid e avançar o foco para o próximo componente da tela utilizando-se as teclas de atalho "Ctrl + Tab".

---

### Versão 2.1.0.5 (03/04/2023)

[SISTEMA]

- Em Gestão de Acesso, melhorias de segurança nos processos de alteração de usuários e níveis de acesso, e restrição de visualização da senha ou alteração do e-mail remetente configurado somente ao nível Administrador.

[CADASTRO]

- Em Unidades Organizacionais, ajustes e correções necessárias.

[CARREIRAS]

- Em Progressões e Concessões Funcionais, ajustes na verificação periódica de alterações no DL ativo realizadas por outros usuários.

[OUTROS]

- Modernização visual dos grids em todas as telas do sistema, com formatação em linhas zebradas.
- Implementação visual para os campos "status" do sistema (Vínculos, Unidades Organizacionais, Remetentes, Listagens etc.) e atualização do design desse campo para Diplomas Legais.
- Correções na rotina de exportação para planilha MS Excel e na janela "Pesquisar Unidade Organizacional".
- Melhorias pontuais de estabilidade e prevenção de bugs.

---

### Versão 2.1.0.4 (10/03/2023)

[SISTEMA]

- Na tela de login, remoção da exibição da data de compilação da versão e melhorias visuais.
- Em Configurações de Sistema, inclusão da configuração de nível de acesso para autorização da efetivação de concessões.
- Melhorias no recurso para visualização rápida dos registros vinculados a um Diploma Legal, através do menu de contexto, selecionando-se a opção "Visualizar", disponível na Tela Principal e outras telas do sistema.
- Em Meu Perfil, distribuição dos campos em abas e inclusão do campo Chave API OpenAI ChatGPT.

[TELA PRINCIPAL]

- No menu de contexto do painel de DLs Abertos, realizadas as seguintes inclusões e melhorias:
  - Remoção das opções de dividir e reunir grupos, relativos aos DLs abertos e ocultos;
  - Inclusão das opções "Aprovar Análise" e "Autorizar Concessão", esta última disponível apenas a usuários com nível de acesso igual ou superior ao configurado no sistema.

[CARREIRAS]

- Em Progressões Funcionais, realizadas as seguintes inclusões e melhorias:
  - Inclusão da opção "Autorizar Concessão", conforme nível de acesso do usuário;
  - Melhorias na verificação periódica de alterações no DL ativo realizadas por outros usuários.
  - Ajuste no filtro de pesquisa para não retornar docentes com RT em concessão, porém com menos de três anos de exercício, não tendo, por consequência, concluído o estágio probatório.
- Em Concessões Funcionais, realizadas as seguintes inclusões e melhorias:
  - Inclusão da opção "Autorizar Concessão", conforme nível de acesso do usuário;
  - Inclusão da opção "Visualiza" Diploma Legal no menu de contexto do grid superior;
  - Melhorias na verificação periódica de alterações no DL ativo realizadas por outros usuários.

[FERRAMENTAS]

- Em Favoritos, inclusão de link para a aplicação FastChatGPT, disponível se presente o arquivo FastChatGPT.dll na pasta "apps", para utilização da plataforma OpenAI ChatGPT, cuja chave API deve estar cadastrada no perfil do usuário ou como variável de ambiente do SO Windows.

[OUTROS]

- Redução de 2 para 1,3 segundos no tempo de exibição da mensagem de alerta de não conectividade com o servidor.
- Melhorias pontuais de estabilidade e prevenção de bugs.

---

### Versão 2.1.0.3 (01/02/2023)

[SISTEMA]

- Na tela de login, remoção da exibição do endereço Internet Protocol (IP) do usuário.

[TELA PRINCIPAL]

- No painel de DLs Abertos, ajustes na exibição dos indicadores de links e de status de aprovação no layout Detalhes.

[CADASTRO]

- Em Cadastro de Diplomas Legais, aprimoramento dos filtros de seleção de DLs com melhoria de performance.
- Em Registro de Ocorrências Funcionais, inclusão da Auditoria de Ocorrências, que analisa a concomitância de ocorrências como licença para tratamento de saúde ou de pessoa da família, faltas não justificadas e similares, no menu de contexto.

[CARREIRAS]

- Em Concessões Funcionais, aprimoramento da pesquisa da concessão vigente e cálculo do adicional percentual para a concessão de Incentivo à Qualificação, ao incluí-la no Diploma Legal.

[FERRAMENTAS]

- Em Integração Sistêmica, na importação de licenças e afastamentos, realizadas as seguintes inclusões e melhorias:
  - Inclusão de verificações de alteração no primeiro dia de licença e existência de licença com período concomitante a outra já cadastrada do mesmo tipo, reduzindo o risco de cadastros em duplicidade;
  - Aprimoramento do processo que agora é realizado com até três etapas: Importação da listagem, Auditória de Ocorrências e Análise de Ocorrências Funcionais, que passa a ser realizada para todos os vínculos e não apenas para os que ainda possuem possibilidade de progressão.

[RELATÓRIOS]

- Em Listagens, realizadas as seguintes inclusões e melhorias:
  - Correção nos somatórios informados na linha Total da listagem Progressões e Concessões Efetivadas;
  - Substituição do filtro de Ocorrências por filtros avançados (opções de seleção) na listagem Ocorrências por Vínculo;
  - Inclusão de dados de consolidação (totais e percentuais) na listagem Diplomas Legais Editados por Assunto.
- Em Relatórios Gerais, no relatório de Progressões e Concessões Efetivadas correção do filtro de critério Vigência no Período, e inclusão de filtro opcional que permite adicionar concessões de Ambiente Organizacional.

[OUTROS]

- Melhorias pontuais de estabilidade e prevenção de bugs.

---

### Versão 2.1.0.2 (10/01/2023)

[SISTEMA]

- Na tela de login, aprimoramento do processo de controle e gestão das conexões disponíveis e do login no sistema.
- Tela "Ferramentas de Banco de Dados" renomeada para "Administração de Banco de Dados".
- Em Administração de Banco de Dados, remoção do limite de conexões registradas com bancos de dados.
- Inclusão do recurso de visualização de uma das seções ocultas do painel principal de botões ao mover-se o mouse sobre o logotipo da instituição, se a configuração de rolagem do painel estiver habilitada.

[TELA PRINCIPAL]

- No painel de DLs Abertos, remoção do cabeçalho no layout Detalhes e inclusão da opção "Ordenar por" no menu de contexto.

[CARREIRAS]

- Em Posicionamentos, realizadas as seguintes inclusões e melhorias:
  - Aprimoramento das ações de pesquisa e filtragem, e inclusão de opções de visualização;
  - Inclusão do filtro dinâmico Anotações Registradas para filtrar apenas os registros que possuem anotações.
- Em Progressões e Concessões Funcionais, realizadas as seguintes inclusões e melhorias:
  - Inclusão do filtro dinâmico Anotações Registradas para filtrar apenas os registros que possuem anotações;
  - Ajuste da transposição de anotações do DL para o histórico de posicionamentos ou concessões, conforme o caso.
- Em Progressões Funcionais, aprimoramento das opções de análise de ocorrências no menu de contexto do grid inferior.

[FERRAMENTAS]

- Em Base de Conhecimento, inclusão do recurso de impressão do registro consultado, com pré-visualização em formato .pdf.

[RELATÓRIOS]

- Em Listagens, inclusão da coluna DL na listagem Progressões e Concessões em Processamento.

[OUTROS]

- Melhorias pontuais de estabilidade e prevenção de bugs.
- Ajustes necessários ao suporte a múltiplos monitores de vídeo.

---

### Versão 2.1.0.1 (20/12/2022)

[SISTEMA]

- Alterações em diversas telas e funções para implementação do recurso de acesso multiunidade/multiorganização.

[TELA PRINCIPAL]

- Novo recurso adicionado para geração de relatório do Diploma Legal, com o respectivo rol de concessões, através do menu de contexto, selecionando-se a opção "Relatório".
- Inclusão de rotina de atualização diária automática da vigência prevista para vínculos que possuem vigente ocorrência que suspende a contagem do interstício atual para a próxima progressão.
- Inclusão de rolagem do painel principal de botões por meio das setas esquerda (left) e direita (right) do teclado.
- Inclusão da ativação de seleção do painel de DLs abertos ao pressionar-se a tecla de seta baixo (down) do teclado (esse recurso inativa temporariamente a rolagem do painel principal de botões, que pode ser reativada pressionando-se a tecla Tab).
- Inclusão de atalhos para alternância entre layout (F4), esconder/mostrar ocultos (F6) e dividir/reunir grupos (F7).
- Atualização dos designs dos ícones.

[CADASTRO]

- Em Cadastro de Diplomas Legais, inclusão da opção "Relatório" do Diploma Legal no menu de contexto.
- Em Cadastro de Pessoas, inclusão de restrições adicionais a depender da unidade logada, vez que esse cadastro é compartilhado entre unidades e instituições distintas.
- Em Contatos (Destinatário), inclusão da possibilidade de restrição de um Grupo/Marcador somente à unidade criadora.

[CARREIRAS]

- Em Progressões e Concessões Funcionais, realizadas as seguintes inclusões e melhorias:
  - Inclusão da verificação, a cada um minuto, de alterações recentes no estado do DL aberto realizadas por outro usuário.
  - Inclusão de filtragem na seleção dos assinantes possíveis para o tipo do DL aberto, conforme previamente configurado em Instituições e Autoridades.
- Tela "Consultas e Posicionamentos" renomeada para "Posicionamentos".
- Em Análise de Ocorrências Funcionais, realizadas as seguintes inclusões e melhorias:
  - Ajustes na rotina do processamento da análise de ocorrências;
  - Inclusão de rotina de verificação das progressões em processamento durante a análise em lote;
  - Inclusão, no menu de contexto, de opção para emissão do relatório "Dossiê do Vínculo";
  - Inclusão, no menu de contexto, de opções para editar ou excluir registro da tela de análise;
  - Inclusão do novo relatório "Análise de Ocorrências Funcionais".

[FERRAMENTAS]

- Em Base de Conhecimento, inclusão da possibilidade de restrição de um registro somente à unidade criadora.
- Tela "Sincronizações Cadastrais" renomeada para "Integração Sistêmica".
- Tela "Notificações Eletrônicas" renomeada para "Central de Notificações".
- Em Favoritos, inclusão da possibilidade de restrição de um favorito somente à unidade criadora.

[RELATÓRIOS]

- Tela "Relatórios Impressos" renomeada para "Relatórios Gerais".

[OUTROS]

- Melhorias pontuais de estabilidade e prevenção de bugs.
- Atualizações das referências às telas renomeadas.
- Atualizações para operacionalização do recurso de acesso multiunidade/multiorganização.

---

### Versão 2.0.0.7 (11/11/2022)

[SISTEMA]

- Inclusão da possibilidade de memorização de mais de um usuário na tela de login.
- Em Ferramentas do Banco de Dados, melhorias no processo de geração de backup, com a inclusão de chaves estrangeiras de acordo com o schema do banco de dados na exportação do arquivo SQL.

[TELA PRINCIPAL]

- Novo recurso adicionado para visualização rápida dos registros vinculados a um Diploma Legal, através do menu de contexto, selecionando-se a opção "Visualização".

[CADASTRO]

- Em Cadastro de Diplomas Legais, inclusão da opção "Visualização" do Diploma Legal no menu de contexto.

[CARREIRAS]

- Em Consultas e Posicionamentos, inclusão da opção "Visualização" do Diploma Legal no menu de contexto do grid inferior.
- Em Análise de Ocorrências Funcionais, realizadas as seguintes inclusões e melhorias:
  - Melhorias com novas opções no menu de contexto da análise em lote, para remoção ou reanálise de vínculos;
  - Ajustes para prevenção de travamentos e bugs.

[OUTROS]

- Disponibilização da emissão do relatório Dossiê do Vínculo nas principais telas do sistema, através do menu de contexto.
- Melhorias pontuais de estabilidade e prevenção de bugs.

---

### Versão 2.0.0.6 (26/10/2022)

[SISTEMA]

- Modernização e melhorias visuais na tela de login.

[CARREIRAS]

- Em Análise de Ocorrências Funcionais, ajustes para melhor tratamento de enquadramento e decisão administrativa e melhorias para prevenção de travamentos na análise.

[FERRAMENTAS]

- Em Sincronizações Cadastrais, em Licenças, após a gravação das novas ocorrências importadas, inclusão de diálogo com opção para reprocessar a análise em lote para os vínculos que ainda não atingiram o topo da carreira.

[OUTROS]

- Melhorias pontuais de estabilidade e prevenção de bugs.

---

### Versão 2.0.0.5 (01/09/2022)

[TELA PRINCIPAL]

- No painel de DLs Abertos, exibição de DLs ainda sem registro vinculado.

[CARREIRAS]

- Em Progressões Funcionais, correção na rotina de análise Progressão (API SIAPE) do grid inferior.

[FERRAMENTAS]

- Em Sincronizações Cadastrais, realizadas as seguintes inclusões e melhorias:
  - No painel de título, inclusão de botão para execução de aplicação externa, eventualmente existente para otimizar o processo de integração ou sincronização cadastral com outros sistemas;
  - Em Licenças, inclusão da opção Analisar Ocorrências no menu de contexto e de funcionalidade para reprocessar a análise após a gravação das novas ocorrências importadas.

[RELATÓRIOS]

- Em Listagens, inclusão da coluna Data 24 Meses na listagem Licenças para Tratamento de Saúde (Controle), que informa a data em que o vínculo atingiu o limite de 24 meses estabelecido pela Lei 8.112/90.
- Em Relatórios Impressos, correção das informações do relatório Progressões e Concessões Efetivadas.

[OUTROS]

- Melhorias pontuais de estabilidade e prevenção de bugs.
- Pastas passar a ter letras minúsculas no diretório de instalação do sistema.

---

### Versão 2.0.0.4 (03/08/2022)

[TELA PRINCIPAL]

- Inclusão, no painel de DLs Abertos, da possibilidade de ordenação dos DLs, ascendente ou descendente, quando o layout em exibição for "Detalhes", através de clique no cabeçalho da respectiva coluna.

[CARREIRAS]

- Em Consultas e Posicionamentos, no painel de atributos do posicionamento, inclusão do atributo Decisão Administrativa.
- Em Análise de Ocorrências Funcionais, realizadas as seguintes inclusões e melhorias:
  - Ajustes na rotina de verificação de inabilitações em avaliação de desempenho quando do processamento realizado a partir de ocorrências cadastradas no sistema;
  - Inclusão de opção de configuração para contagem cumulativa ou não de ocorrências com inabilitações em avaliação de desempenho justapostas;
  - Ajustes para o tratamento do atributo Decisão Administrativa no processamento da análise.
- Em Progressões Funcionais, inclusão de funcionalidades para o tratamento do atributo Decisão Administrativa, para algumas progressões cuja vigência informada diverge da vigência prevista, e opção de alteração do atributo em Alterar Posicionamento.

[FERRAMENTAS]

- Em Sincronizações Cadastrais, melhoria da funcionalidade de importação de vínculos, para importação daqueles devidamente posicionados na carreira, porém com situação funcional "excedente a lotação".

[RELATÓRIOS]

- Em Relatórios Impressos, inclusão de configurações adicionais: (a) descaracterização de dados pessoais, tais como matrícula, CPF e e-mail; e (b) visualização em fluxo contínuo, que gera a pré-visualização do relatório em página única.

[OUTROS]

- Melhorias pontuais de estabilidade e prevenção de bugs.

---

### Versão 2.0.0.3 (22/07/2022)

[SISTEMA]

- Na tela de login, inclusão de mensagem de Caps Lock ativado, para equipamentos que não possuem LED indicador.
- Inclusão de ícone com recursos úteis na barra de tarefas do sistema operacional MS Windows.
- Em Preferências do Usuários, inclusão de configuração que permite definir o layout de exibição dos DLs Abertos ao iniciar.

[TELA PRINCIPAL]

- Inclusão, no menu de contexto, de seleção entre as opções "Ícones" e "Detalhes" para o layout de exibição dos DLs Abertos.

[CARREIRAS]

- Em Concessões Funcionais, inclusão da funcionalidade de inserção de registro histórico de concessões não vinculadas a um DL.

[FERRAMENTAS]

- Em Notificações Eletrônicas, inclusão da funcionalidade de importação de relatório como anexo do e-mail (será aberta a tela de Relatórios Impressos para configuração e geração do relatório, e, ao fechar a visualização do relatório e retornar à tela de Notificações, este será incluído na lista de anexos).
- Em Sincronizações Cadastrais, melhoria da funcionalidade de importação de licenças e afastamentos.

[RELATÓRIOS]

- Em Listagens, realizadas as seguintes inclusões e melhorias:
  - Inclusão de funcionalidade de consulta de vínculo, ocorrências, posicionamentos e concessões do vínculo;
  - Inclusão de funcionalidade de análise de ocorrências funcionais, no menu de contexto, para alguns tipos de listagem;
  - Nova Listagem adicionada relativa ao controle de licenças para tratamento de saúde, para verificação da proximidade do limite estabelecido pela Lei 8.112/90.
- Inclusão de novo relatório do tipo Relatórios Impressos, para a geração de relatórios predefinidos em formato PDF, com os seguintes tipos de relatórios: Posicionamento Atual e Previsão de Progressão; Progressões e Concessões com Pendências;
  Progressões e Concessões Efetivadas; e Dossiê do Vínculo.

[OUTROS]

- Melhorias pontuais de estabilidade e prevenção de bugs.

---

### Versão 2.0.0.2 (01/07/2022)

[TELA PRINCIPAL]

- Melhoria de desempenho na rolagem do painel principal de botões por meio do mouse.
- Inclusão de teclas de atalho para Minhas Anotações (F2) e Atualizar Área de Trabalho (F5).
- Reativação da funcionalidade de maximização da tela.
- Inclusão de indicação visual nas pastas dos DLs cujas análises estejam todas aprovadas, conforme preferências do usuário.

[SISTEMA]

- Em Ferramentas do Banco de Dados, realizadas as seguintes inclusões e melhorias:
  - Inclusão de botão para geração de arquivo SQL com a estrutura do banco de dados;
  - Inclusão de recurso de salvamento temporário dos registros pendentes de sincronização para posterior sincronização.
- Em Preferências do Usuários, inclusão da configuração que permite exibir ou ocultar indicação visual nas pastas dos DLs cujas análises estejam todas aprovadas.

[CARREIRAS]

- Em Progressões e Concessões Funcionais, inclusão de teclas de atalho para operações de análise (F3 e F4), filtragem (F5 e F6) e consultas diversas sobre o vínculo selecionado (F7 a F12).

[FERRAMENTAS]

- Em Notificações Eletrônicas, realizadas as seguintes inclusões e melhorias:
  - Implementação de assinatura pela tag "<USER-ASSIGN>"::000, a ser substituída pelo nome e sobrenome do usuário, e de caracteres sublinhados na quantidade especificada (ex.: <USER-ASSIGN>::045), se a fonte estiver assim formatada;
  - Inclusão de botão para exibição de caixa de diálogo com informações sobre as tags disponíveis para utilização.

[OUTROS]

- Melhorias pontuais de estabilidade e prevenção de bugs.
- Melhorias na performance de consultas de progressões, concessões e posicionamentos de vínculos especificados, bem como na tela de pesquisa de vínculo que passa a exigir ao menos 4 caracteres digitados para realizar a consulta ao banco de dados.
- Ampliação da disponibilidade do recurso Minhas Anotações nas principais telas do sistema, por meio de tecla de atalho (F2).

---

### Versão 2.0.0.1 (03/06/2022)

[SISTEMA]

- Evolução para nova versão, com uma nova identidade mais moderna e original, incluindo novo nome: Evolke.
- Alterações visuais na tela de login, como consequência da nova identidade do sistema.
- Em Meu Perfil, inclusão de campo para cadastro da Chave API do Portal Transparência do Governo Federal.

[TELA PRINCIPAL]

- Alterações visuais e funcionais significativas sobre em relação à lista de Diplomas Legais abertos e à tela em geral.
- Desativação da funcionalidade de maximização da tela devido a restrições de compatibilidade visual com diferentes estilos nas versões do sistema operacional MS Windows.

[CADASTRO]

- Em Cadastro de Pessoas, inclusão de função que emite um alerta caso o CPF informado seja inválido.
- Em Cadastro de Vínculos, inclusão de função de consulta ao posicionamento SIAPE e exercício de função comissionada, conforme última atualização constante do Portal da Transparência do Governo Federal.
- Implementação de novo tipo de cadastro: Cadastro de Instituições Externas;
- Em Cadastro de Diplomas Legais, implementação de campo que permite vinculação de um DL a uma instituição externa.
- Em Cadastro de Remetentes, devido a restrições de autenticação SMTP por alguns provedores ou contas de e-mail, inclusão de campo Alias, isto é, um e-mail que será utilizado como máscara e que será aquele visível ao destinatário.

[CARREIRAS]

- Em Consultas e Posicionamentos, Análise de Ocorrências Funcionais e em Concessões Funcionais, inclusão de função de consulta ao posicionamento SIAPE e exercício de função comissionada, conforme última atualização constante do Portal da Transparência do Governo Federal.
- Em Progressões Funcionais, realizadas as seguintes inclusões e melhorias:
  - Inclusão de função de consulta ao posicionamento SIAPE e exercício de função comissionada, e, também, função de análise da progressão atual registrada no sistema e o posicionamento SIAPE, conforme última atualização constante do Portal da Transparência do Governo Federal;
  - Inclusão, no grid principal, da opção de selecionar vínculos/progressões que já não estejam em processamento.

[FERRAMENTAS]

- Em Notificações Eletrônicas, realizadas as seguintes inclusões e melhorias:
  - Ajustes na inclusão de vínculo como destinatário de maneira a possibilizar a seleção de vários vínculos a serem incluídos como destinatários simultaneamente.
  - Ajustes para utilização de alias, isto é, e-mail informado como máscara que será visível ao destinatário.

[RELATÓRIOS]

- Em Listagens, inclusão da possibilidade de envio de notificação eletrônica para aniversariantes, docentes sem titulação necessária para progredir e servidores em débito (concessões e progressões pendentes).
- No Dashboard, inclusão do filtro Tipo, que permite a distinção de tipos de progressões de uma mesma carreira.

[OUTROS]

- Melhorias pontuais de estabilidade e prevenção de bugs.

---

### Versão 1.0.0.24 (05/04/2022)

[SISTEMA]

- Na tela de login, inclusão de verificação da senha, que deve ser alterada a cada dois anos.
- Em Meu Perfil, inclusão de restrições e orientações para a definição de senha pelo usuário, para maior segurança.

[TELA PRINCIPAL]

- Inclusão de teclas de atalho para os principais recursos, com Shift + letra. Por exemplo, Shift + D acessa o Cadastro de Diplomas Legais; Shift + P acessa a tela de Planejamento e Controle de Progressões Funcionais etc.
- Nova forma de acesso ao menu do sistema como menu suspenso por meio do clique com o botão direito do mouse sobre a área imediatamente abaixo da barra de títulos do sistema.

[CARREIRAS]

- Em Consultas e Posicionamentos, inclusão de opção de exclusão de posicionamento histórico, para usuários com perfil de gestor júnior ou superior.
- Em Progressões e Concessões Funcionais, inclusão de botão para acesso ao URL do DL em visualização, se disponível.
- Em Concessões Funcionais, inclusão de procedimento que verifica e, se necessário, atualiza a previsão de Aceleração da Promoção quando da concessão de Retribuição por Titulação a docentes ainda em período de estágio probatório.

[FERRAMENTAS]

- Em Notificações Eletrônicas, assuntos agora apresentados em ordem alfabética.

[OUTROS]

- Melhorias pontuais diversas de estabilidade e prevenção de bugs.
- Expressão "estimativa" relacionada a vigência de progressões futuras a realizar alteradas para "previsão".

---

### Versão 1.0.0.23 (31/01/2022)

[SISTEMA]

- Na tela de login, ajuste da funcionalidade de verificação de atualização obrigatória pendente, para os casos em que um usuário esteja utilizando uma versão antiga e exista versão posterior obrigatória.

[CARREIRAS]

- Em Progressões Funcionais, realizadas as seguintes inclusões e melhorias:
  - Ajustes para possibilitar análise de ocorrências em lote, com os vínculos selecionados;
  - Inclusão das opções "Selecionar Tudo" e "Analisar Ocorrências" no grid inferior, com os registros incluídos na minuta de DL.
- Em Análise de Ocorrências Funcionais, diversos ajustes para possibilitar análise de ocorrências em lote, de maneira que a partir de agora, existem dois modos de análise possíveis (Individual e Em Lote), podendo haver alternância entre ambos; cada modo utiliza um arquivo .CSV distinto a ser importado.

[FERRAMENTAS]

- Em Base de Conhecimento, inclusão de menu de contexto para o botão Pesquisar, através do clique com o botão direito do mouse, com as opções "Pesquisar em Tudo" e "Abrir toda a Base".

[OUTROS]

- Melhorias pontuais diversas de estabilidade e prevenção de bugs.

---

### Versão 1.0.0.22 (29/12/2021)

[TELA PRINCIPAL]

- Inclusão de funcionalidade de rolagem das seções de botões, com o uso do mouse, disponível por padrão caso não esteja desabilitada em Preferências do Usuário.

[SISTEMA]

- Em Preferências do Usuários, realizadas as seguintes inclusões e melhorias:
  - Inclusão da configuração que permite exibir ou ocultar mensagens de exceções e erros do sistema - por padrão, a exibição de mensagens é ocultada, apenas gerando o respectivo log;
  - Inclusão da configuração que habilita ou desabilita a rolagem das seções de botões na Tela Principal.

[CADASTRO]

- Em Cadastro de Vínculos, inclusão de máscara para restrição de acesso a informações pessoais de matrícula SIAPE e e-mail, para usuários com perfil de acesso Convidado ou equivalente.
- Em Cadastro de Diplomas Legais, inclusão da funcionalidade Edição Rápida em Lote, para rápida alteração dos números e URLs de vários DLs, através do clique com o botão direito do mouse.
- Em Instituições e Autoridades, realizadas as seguintes inclusões e melhorias:
  - Implementação da opção de cadastro de substitutos legais;
  - Inclusão de opção de exclusão de DL, Autoridade, Cargo e Instituição, para usuários com perfil de gestor pleno ou superior.

[CARREIRAS]

- Em Progressões e Concessões Funcionais, inclusão da opção de seleção da autoridade assinante na edição de Portaria, nos casos em que houver mais de uma autoridade cadastrada, incluindo substitutos legais.
- Em Análise de Ocorrências Funcionais, ajuste no carregamento automático de arquivo .CSV existente para que seja perguntado ao usuário se deseja carregar o arquivo existente.

[RELATÓRIOS]

- Liberação do Relatório Listagens para usuários com perfil de acesso Convidado ou equivalente; porém, com restrição à visualização de listagens específicas que, potencialmente, contenham informações pessoas.
- Inclusão de filtro de ocorrências selecionadas na listagem Ocorrências por Vínculo.

[OUTROS]

- Melhorias pontuais diversas de estabilidade e prevenção de bugs.
- Em variadas telas do sistema, inclusão de máscara para restrição de acesso a informação pessoal de matrícula SIAPE, para usuários com perfil de acesso Convidado ou equivalente.

---

### Versão 1.0.0.21 (05/11/2021)

[TELA PRINCIPAL]

- Inclusão no botão de verificação com informações sobre status e desempenho da conexão do sistema com o servidor, do recurso de seleção do modo de teste de conexão entre ICMPIndy (com RAW Socket) e ICMPSendEcho (sem RAW Socket), esta última para dispensar a necessidade de permissão de Administrador exigida pela API do SO Windows que utiliza RAW Socket.

[CADASTRO]

- Em Cadastro de Contatos/Destinatários, inclusão de botão para importação de dados do contato em edição ou inserção a partir de vínculo ou unidade organizacional.

[CARREIRAS]

- Em Progressões Funcionais, melhoria na visualização de observações sobre ocorrências e anotações relacionadas ao vínculo selecionado e/ou ao vínculo selecionado incluído em Diploma Legal, incluindo Ambiente Organizacional de servidor TAE.
- Em Concessões Funcionais, inclusão da visualização de Ambiente Organizacional de servidor TAE ao manter o cursor do mouse sobre o botão para consulta a dados do vínculo selecionado (dados cadastrais, ocorrências e posicionamentos).
- Em Progressões e Concessões Funcionais, realizadas as seguintes inclusões e melhorias:
  - Inclusão do botão "Abrir Nova Janela" na barra superior;
  - Inclusão menu popup no botão "Carregar DL", por meio do clique com o botão direito do mouse, com a possibilidade de rapidamente recarregar/atualizar o DL carregado ou, então, carregar outro DL em uma nova janela, com vistas a possibilitar a edição rápida ou consulta de outro DL sem a necessidade de cancelar a edição ou fechar o DL atualmente carregado;
  - Ao carregar um DL, sua descrição aparece na barra de títulos da janela.

[FERRAMENTAS]

- Em Notificações Eletrônicas, implementação de funcionalidade para tratamento da tag <QRCODE-MSG> a ser substituída pelo texto "Caso seja útil, disponibilizamos QR Code em anexo para acesso ao diploma legal em dispositivo móvel.", através da opção "Adicionar por Diploma Legal", caso presente no modelo de notificação e se houver QR Codes dos DLs incluídos para envio.

[RELATÓRIOS]

- Em Listagens, melhorias pontuais e inclusão de pesquisa por unidade de lotação na listagem Aniversariantes do Mês.

[OUTROS]

- Melhorias pontuais diversas de estabilidade e prevenção de bugs.
- O modo de teste de conexão selecionado pelo usuário fica armazenado localmente.

---

### Versão 1.0.0.20 (14/10/2021)

[SISTEMA]

- Na tela de login, inclusão de funcionalidade de verificação de atualização obrigatória pendente, para os casos em que uma nova atualização disponível for obrigatória para o correto funcionamento do sistema, sem a qual não será possível acessar o sistema.

[TELA PRINCIPAL]

- Ajuste na listagem de DLs abertos para tratamento correto de DL do tipo "Retribuição por Titulação/Aceleração da Promoção".

[CADASTRO]

- Em Cadastro de Diplomas Legais, inclusão do assunto "Retribuição por Titulação/Aceleração da Promoção", para vinculação da concessão de RT e da AP a um único DL.
- Em Cadastro de Diploma Legal, inclusão da funcionalidade de geração de QR Code a partir do link URL do DL.

[CARREIRAS]

- Em Progressões e Concessões Funcionais, ajustes necessários ao tratamento correto de DL do tipo "Retribuição por Titulação/Aceleração da Promoção".
- Em Progressões Funcionais, inclusão de botão de acesso à concessões para o vínculo selecionado, através do clique com o botão direito do mouse.
- Em Consultas e Posicionamentos e em Concessões Funcionais, inclusão da funcionalidade de geração de QR Code a partir do link URL do DL.

[FERRAMENTAS]

- Em Notificações Eletrônicas, implementação da funcionalidade de inclusão automática de QR Codes dos DLs incluídos para envio, através da opção "Adicionar por Diploma Legal", nos casos em que o DL possui link URL.

[RELATÓRIOS]

- Em Listagens e Relatórios Gráficos, ajustes necessários ao tratamento correto de registros e DLs relacionados a "Retribuição por Titulação/Aceleração da Promoção".

[OUTROS]

- Melhorias pontuais diversas de estabilidade e prevenção de bugs.

---

### Versão 1.0.0.19 (03/09/2021)

[SISTEMA]

- Em Preferências de Exibição do Usuários, inclusão de novas configurações de preferência:
  - Sensibilidade da ativação do menu lateral após o movimento do mouse sobre o menu;
  - Configuração das seções visíveis preferenciais do usuário na Tela Principal quando a tela estiver em estado normal;
  - Configuração da visibilidade das anotações do usuário na Tela Principal;
  - Configuração da visibilidade da quantidade de registros - concessões ou progressões - vinculados aos DLs abertos.
- Inclusão de mecanismo de verificação constante da conectividade do sistema com o servidor do banco de dados.

[TELA PRINCIPAL]

- Tempo para ativação do menu lateral após o movimento do mouse sobre o menu, conforme preferência do usuário.
- Possibilidade de configuração das seções visíveis preferenciais do usuário quando a tela estiver em estado normal.
- Possibilidade de configuração da visibilidade das anotações do usuário (se o número de DLs abertos for superior ao limite visível quando a tela estiver em estado normal, as anotações serão ocultadas automaticamente).
- Inclusão de botão de verificação com informações sobre status e desempenho da conexão do sistema com o servidor.
- Inclusão de mecanismo automático de pesquisa dos DLs abertos a cada 10 minutos, aproximadamente, com vistas a atualizar a listagem para os usuários logados.
- Novas opções de formatação das anotações do usuário: ajuste de texto, tamanho da fonte e tipo de fonte.
- Inclusão da visibilidade da quantidade de registros - concessões ou progressões - vinculados aos DLs abertos ao passar o mouse sobre esses DLs, conforme preferências do usuário.

[CADASTRO]

- Em Cadastro de Vínculos, ajuste na operação de gravação do vínculo para melhor tratamento dos casos de transformação de vínculo de outro tipo para o tipo estatutário, como nos casos de servidor em exercício provisório que obteve a redistribuição tornando-se servidor efetivo do órgão. Nesses casos, não se deve cadastrar um novo vínculo, mas alterar o tipo do vínculo. Com isso, serão criados os devidos registros de posicionamentos e progressão na carreira.

[CARREIRAS]

- Em Concessões Funcionais, inclusão de botão para consulta a dados do vínculo selecionado (dados cadastrais, ocorrências e posicionamentos).
- Em Análise de Ocorrências Funcionais, inclusão de opção de análise que, para os docentes, faz prevalecer a Promoção por Avaliação de Desempenho em lugar da Aceleração da Promoção automática com base na titulação atual, exceto se o posicionamento estiver registrado com o atributo posicionamento por titulação.

[FERRAMENTAS]

- Em Base de Conhecimento, inclusão da opção de colar texto sem formatação, quando em inserção ou edição; inclusão da opção de formatação ajuste de texto; e correções e melhorias gerais de utilização e pesquisa.
- Em Notificações Eletrônicas, inclusão da opção de formatação ajuste de texto; e melhorias gerais de utilização.
- Inclusão da nova ferramenta Favoritos, voltada ao armazenamento, consulta e pesquisa rápida de links favoritos, similar à funcionalidade existente nos navegadores de internet.

[OUTROS]

- Inclusão do botão Favoritos na barra superior de diversas telas do sistema, para acesso rápido a esse recurso.
- Inclusão do botão Limpar Filtros na barra superior de diversas telas do sistema, em que haja barra de pesquisa.
- Novas opções de formatação das anotações: ajuste de texto, tamanho da fonte e tipo de fonte.
- Melhorias pontuais diversas de estabilidade e prevenção de bugs.

---

### Versão 1.0.0.18 (28/07/2021)

[SISTEMA]

- Adição de opções de configurações para a realização de backup do banco de dados em arquivos SQL.
- Em Preferências de Exibição do Usuários, inclusão de novas configurações de preferência:
  - Estado inicial da tela principal - normal ou maximizada - e, se em estado normal, ajuste de posicionamento no monitor;
  - Opção do menu principal - recolhido ou expandido - para cada estado da tela principal - normal ou maximizada.

[CARREIRAS]

- Em Consultas e Posicionamentos, inclusão de painel com informações sobre os atributos enquadramento e posicionamento por titulação do posicionamento histórico; e inclusão de botões para as telas Listagens, Gráficos e Base de Conhecimento.
- Em Progressões e Concessões Funcionais, substituição do botão para a tela Estruturas de Carreiras pelo botão para a tela Base de Conhecimento.

[FERRAMENTAS]

- Em Notificações Eletrônicas, inclusão da formatação de texto para escolha da fonte (via de regra, a fonte padrão é Tahoma); e botão para a tela Base de Conhecimento.
- Inclusão da nova ferramenta Base de Conhecimento, voltada ao armazenamento, consulta e pesquisa de orientações, decisões e normativas internas e externas, por assunto e/ou termos de pesquisa (para pesquisa com vários termos, utilizar "&&", sem aspas, entre os termos a pesquisar).

[OUTROS]

- Melhorias pontuais diversas de estabilidade e prevenção de bugs.

---

### Versão 1.0.0.17 (05/07/2021)

[SISTEMA]

- Na tela de login, realizadas as seguintes alterações ou melhorias:
  - Ajustes para alternância entre os controles (botões e campos) da tela por meio da tecla TAB;
  - Implementação das setas direcionais esquerda e direita para seleção do banco de dados;
  - Implementação das teclas de atalho para o acesso como convidado (Alt+A) ou à tela de recuperação de senha (Alt+E).
- Implementação da desabilitação temporária do som de beep do SO Windows durante a execução do sistema.

[CADASTRO]

- Em Cadastro de Vínculos, ajuste do início da Progressão por Capacitação de TAE para 01/03/2005 quando do cadastro de um servidor TAE que entrou em exercício antes dessa data, haja vista tal tipo de progressão ter sido instituído somente em tal data, conforme Lei nº 11.091/2005.

[FERRAMENTAS]

- Em Notificações Eletrônicas, inclusão da possibilidade de inserção, no corpo do e-mail, de listagem de vínculos com matrícula e nome, por meio da expressão-chave "<MAT-VINCULO> - <NOME-VINCULO> - <TIT-VINCULO> - <NUMPROC>", o que permite a criação de um modelo de e-mail para informação acerca de um rol de vínculos selecionados.
- Em Notificações Eletrônicas, inclusão da funcionalidade de maximizar/restaurar a tela.

[RELATÓRIOS]

- No Dashboard, inclusão do filtro Ano de Referência, que permite consulta aos indicadores relativos ao ano anterior e comparação com o ano corrente; especialmente útil quando o último processamento de concessões e progressões de um ano ocorrer no início do ano seguinte.

[OUTROS]

- Melhorias pontuais diversas de estabilidade e prevenção de bugs.

---

### Versão 1.0.0.16 (11/06/2021)

[SISTEMA]

- Em Preferências de Exibição do Usuário, inclusão da opção de exportação para planilha OpenOffice (BR Office ou Libre Office) em alternativa ao MS Excel, para as situações em que o MS Excel esteja indisponível ou com limitações de uso em função de cópia não registrada ou com licença expirada. Atenção: para importações de arquivos .xls ou .csv, o sistema continua utilizando do pacote Office definido pelo usuário como padrão nas configurações do SO Windows.

[TELA PRINCIPAL]

- Correção do efeito de dois cliques simples quando do duplo-clique sobre um DL.
- Ajustes na rotina de exibição do menu lateral para compatibilidade com o SO Windows 7.
- Remoção do menu popup da listagem de DLs abertos, anteriormente acessado pelo clique com o botão direito do mouse.

[RELATÓRIOS]

- No Dashboard, inclusão de botão de acesso a listagens e relatórios gráficos.

[OUTROS]

- Ajustes na rotina de exportação para planilhas eletrônicas nas telas onde houver para exportação para planilha OpenOffice, se escolhido pelo usuário.
- Melhorias pontuais diversas de estabilidade e prevenção de bugs.

---

### Versão 1.0.0.15 (01/06/2021)

[TELA PRINCIPAL]

- Reestilização da tela principal com visual moderno e limpo, menu lateral dinâmico - tecla de atalho Alt+M, se necessário - e opção de maximização.

[CADASTRO]

- Inclusão de opção alternativa para ocorrência Afastamento para Mandato Eletivo para Vereador, quando houver compatibilidade de horário, hipótese que não interrompe interstício para progressão/promoção.

[CARREIRAS]

- Em Análise de Ocorrências Funcionais, ajustes para tratamento adequado do Afastamento para Mandato Eletivo para Vereador, quando houver compatibilidade de horário.
- Em Progressões Funcionais, realizadas as seguintes alterações ou melhorias:
  - Ajustes na "Aceleração da Promoção", de modo a estimar a vigência da próxima progressão com base na titulação;
  - Inclusão de opção para marcação de progressão pendente, similar à existente para concessões funcionais.
- Em Progressões Funcionais, ajuste na efetivação da RSC para atualização da titulação do vínculo com base na RSC concedida.

[RELATÓRIOS]

- Alteração da listagem Concessões Funcionais Pendentes para Progressões e Concessões Funcionais Pendentes, de modo a apresentar progressões marcadas com pendência.
- No Dashboard, inclusão de novos indicadores de gestão de carreiras: Tempo Médio de Pendências em Promoções e Progressões (TMPP) e Taxa de Promoções e Progressões Concedidas (TxPC).

[OUTROS]

- Melhorias pontuais diversas de estabilidade e prevenção de bugs.

---

### Versão 1.0.0.14 (11/05/2021)

[TELA PRINCIPAL]

- Inclusão de botão de acesso ao relatório Dashboard na barra de menus.

[CADASTRO]

- Em Diplomas Legais, inclusão da possibilidade de anotações para o DL.
- Em Remetentes, inclusão da possibilidade de exclusão de remetente.
- Inclusão do cadastro de Contatos/Destinatários com funcionalidade de atribuição de grupo/marcador.
- Bloqueio do acesso ao cadastro de Ocorrências Funcionais para usuário Convidado, em função da LGPD.

[CARREIRAS]

- Em Consultas e Posicionamentos, inclusão dos atributos de "enquadramento" e/ou "posicionamento por titulação" para um posicionamento cadastrado. Ambos são objeto de análise na Análise de Ocorrências Funcionais. Ao contrário do posicionamento por titulação, o enquadramento não altera a estimativa de vigência da próxima progressão.
- Em Progressões Funcionais, ao se efetivar progressões com DL relativo a "Aceleração da Promoção", o atributo "posicionamento por titulação" é marcado no histórico para essas progressões.
- Em Análise de Ocorrências Funcionais, realizadas as seguintes alterações ou melhorias:
  - Bloqueio da análise para usuário Convidado, em função da LGPD;
  - A análise passa a tratar os históricos de "enquadramento" e/ou "posicionamento por titulação";
- Nas telas onde houver, a consulta à Estrutura Mínima de Carreira passa a tratar os históricos de "enquadramento" e/ou "posicionamento por titulação".

[FERRAMENTAS]

- Em Notificações Eletrônicas, inclusão da possibilidade de seleção de vários Diplomas Legais, com sua listagem no corpo do e-mail em substituição à expressão-chave "<DL-NUM/ANO> - <DL-ASSUNTO>.", o que permite a criação de um modelo de e-mail para informação acerca de um rol de DLs selecionados.
- Em Notificações Eletrônicas, inclusão da possibilidade de seleção de contatos cadastrados individualmente ou por grupo/marcador.
- Em Sincronizações Cadastrais, melhoria na sincronização de vínculos para verificação em conjunto de alterações de e-mail e lotação, se a opção for marcada pelo usuário.

[RELATÓRIOS]

- Inclusão de novo relatório do tipo Dashboard (utilize as opções de maximizar e restaurar janela para melhor visualização).
- Nova Listagem adicionada relativa às concessões pendentes para melhor controle da entrega de diplomas ou outras pendências.

[OUTROS]

- Inclusão de configuração que habilita a visualização de efeitos financeiros quando este recurso estiver desabilitado no sistema.
- Melhorias pontuais diversas de estabilidade e prevenção de bugs.

---

### Versão 1.0.0.13 (18/03/2021)

[TELA PRINCIPAL]

- Inclusão dos botões de atalho Atualizar Listagem e Ocultar/Exibir Anotações.

[CADASTRO]

- Ajustes e melhorias no cadastro de Unidades Organizacionais, com inclusão dos campos e-mail, telefone e dirigente.
- Em Diplomas Legais, inclusão da possibilidade de exclusão de DL sem vinculações, para usuários com perfil de administrador.
- Ajustes no cadastro de Instituições e Autoridades.
- Em Ocorrências Funcionais, inclusão da possibilidade de exclusão de ocorrência, para usuários com perfil de administrador.

[CARREIRAS]

- Em Progressões Funcionais, Concessões Funcionais e Consultas e Posicionamentos, melhoria no filtro de pesquisa por unidades organizacionais, de modo a permitir a filtragem incluindo subunidades das unidades selecionadas.
- Em Progressões e Concessões Funcionais, inclusão:
  - da opção de Consultar Diploma Legal, se existente;
  - de campo para inclusão dos efeitos financeiros;
  - de mecanismo de verificação de progressões ou concessões em processamento, para evitar duplicidade; e,
  - de botões de consulta às telas relatórios em listagens, relatórios gráficos e estruturas de carreiras.
- Em Progressões Funcionais, ajuste na pesquisa de docentes com filtro de titulação requerida habilitado, para incluir aqueles com concessão de nova RT, com DL aberto, cuja nova titulação atenda à titulação requerida.

[FERRAMENTAS]

- Em Sincronizações Cadastrais, ajuste na rotina de geração de lista de e-mails com a inclusão da funcionalidade de marcação ou desmarcação de e-mail a ser exportado para arquivo de texto (.doc).
- Em Notificações Eletrônicas, inclusão de: opção de seleção de vínculos por Unidades Organizacionais de lotação; opção de seleção dos contatos de dirigentes e secretarias de Unidades Organizacionais; contador de destinatários selecionados; e identificação do tipo de designação do vínculo (técnico ou docente).

[RELATÓRIOS]

- Ajuste na listagem Unidades Organizacionais e Quantitativos para a correta agregação dos quantitativos de vínculos lotados nas unidades hierarquicamente inferiores a cada unidade, organizado pelo identificador.
- Nova Listagem adicionada relativa às Progressões e Concessões em processamento, considerando os DLs abertos.
- Em Relatórios Gráficos, inclusão da possibilidade de seleção do exercício (ano) para alguns gráficos em que o exercício de análise estava restrito ao exercício corrente. Os gráficos relativos a exercícios anteriores serão tão precisos quanto estiverem completos os cadastrados de vínculos e concessões funcionais.

[OUTROS]

- Na tela Pesquisar Unidade Organizacional, inclusão de checkbox para seleção de unidades hierarquicamente inferiores.
- Em Informações, inclusão da funcionalidade de impressão do histórico de versões do sistema para arquivo de texto (.txt).
- Inclusão da opção de habilitação/desabilitação, para todo o sistema, do recurso opcional de distinção entre vigência e efeitos financeiros, prevalecendo sobre as preferências de usuários eventualmente configuradas.
- Melhorias pontuais diversas de estabilidade e prevenção de bugs.

---

### Versão 1.0.0.12 (03/02/2021)

[CADASTRO]

- No Cadastro de Diplomas Legais, inclusão do campo DL Oculto, que permite cadastrar DLs com previsão de publicação futura e oculta-los na tela principal - recurso ideal para a preparação de progressões e concessões que ainda estejam aguardando o interstício. DLs ocultos são destacados na cor cinza.

[CARREIRAS]

- Em Progressões e Concessões Funcionais, inclusão da funcionalidade Alterar DL Vinculado, o que permite movimentar progressões ou concessões entre DLs distintos, desde que ambos estejam abertos.
- Em Progressões Funcionais, ajustes na pesquisa de ocorrências do vínculo após o clique no vínculo para mostrar mais de uma ocorrência, se houver.
- Em Análise de Ocorrências Funcionais, ajustes na rotina de cálculo de vigências para a correta análise de ocorrências relativas a mandato eletivo, conforme previsto no art. 38 da CF/88.

[FERRAMENTAS]

- Em Sincronizações Cadastrais, ajustes na rotina de importação de licenças para inclusão da importação de ocorrências relativas a mandato eletivo.

[RELATÓRIOS]

- Ajuste na listagem Cargos e Quantitativos para que se quantifique apenas os vínculos ativos.

[OUTROS]

- Nas telaPesquisar DL, DLs ocultos são destacados na cor cinza.
- Melhorias pontuais diversas de estabilidade e prevenção de bugs.

---

### Versão 1.0.0.11 (12/01/2021)

[CARREIRAS]

- Em Progressões e Concessões Funcionais, inclusão da funcionalidade de consulta de vínculos, ocorrências e posicionamentos para os vínculos incluídos no DL (Grids inferiores).
- Em Progressões Funcionais, melhorias nos filtros de pesquisa para possibilitar o tratamento de vínculos inativos; e ajuste na rotina de concessão de aceleração da promoção, para se verificar se há concessão de nova RT, com DL aberto, que implique em posicionamento distinto ao previsto.
- Em Análise de Ocorrências Funcionais, ajustes na rotina de cálculo de vigências para prevenção de erros e diferenciação da previsão de aceleração da promoção entre as carreiras de Magistério Superior e EBTT; e ajuste na contagem de meses de inabilitação em avaliação de desempenho, de modo a permitir flexibilidade, conforme cadastrado na ocorrência.

[FERRAMENTAS]

- Em Notificações Eletrônicas, ajustes na rotina de envio de e-mail, para melhor tratamento de situações de falhas de envio e envio de grande número de destinatários (centenas ou milhares).
- Em Sincronizações Cadastrais, inclusão da função de Notificação Eletrônica na importação de e-mails, opção "Gerar Lista".
- Em Sincronizações Cadastrais, ajustes na rotina de importação do arquivo .xls para importação do relatório de escolaridade.

[RELATÓRIOS]

- Nova Listagem adicionada relativa aos totais de Progressões e Concessões realizadas, com filtro por ano.

[OUTROS]

- Inclusão da possibilidade de se desativar temporariamente a checagem de conexão com o servidor.

---

### Versão 1.0.0.10 (11/12/2020)

[TELA PRINCIPAL]

- Inclusão de botão para acesso à tela de Concessões Funcionais, se disponível.
- Melhorias de estabilidade e prevenção de erros na pesquisa automática de DLs abertos.

[CADASTRO]

- Inclusão de dois novos assuntos de Diplomas Legais: Ambiente Organizacional e RSC.
- Ajustes na exportação da estrutura de Unidades Organizacionais para imagem bitmap (.bmp).
- Em Instituições, inclusão do cadastro de cabeçalho (formato .png) para Edição de Portaria (MS Word).

[CARREIRAS]

- Inclusão das funcionalidades de anotações e controle de status da análise das progressões incluídas no DL (Grid inferior).
- Inclusão da funcionalidade e respectiva tela de Concessões Funcionais, para controle e preparação de portarias de concessões de IQ, RT e RSC, e de atribuição de Ambiente Organizacional.
- Inclusão das rotinas para Edição de Portaria (MS Word) relacionadas às Concessões Funcionais.
- Alterações da estrutura de dados do campo NOTAS/ANOTAÇÕES para permitir formatação de texto e o armazenamento dessa formatação no banco de dados.

[FERRAMENTAS]

- Em Notificações Eletrônicas, ajustes para listagem dos contatos de portarias relativas a Concessões Funcionais, quando importadas.
- Em Sincronizações Cadastrais, melhoria na inclusão de novo Vínculo para importação automática da unidade de lotação a partir do arquivo importado (.xlsx), em conformidade com as correlações de unidades já cadastradas.
- Em Sincronizações Cadastrais, melhoria na sincronização de Vínculo, para verificar e atualizar nomes dos servidores, quando houver alteração.

[RELATÓRIOS]

- Nova Listagem adicionada relativa às Concessões Funcionais (IQ, RT, RSC e Ambiente Organizacional).
- Ajustes na listagem "Diplomas Legais Editados por Assunto" para contagem dos DLs de Concessões Funcionais.
- Novo Relatório Gráfico adicionado relativa às Concessões Funcionais efetivadas no ano.

[OUTROS]

- Nas telas de pesquisa de Diplomas Legais, inclusão de filtro por período de tempo.
- Registro da data do último login e versão instalada do CCDPSYS no computador do usuário, de forma a permitir ao administrador do sistema melhor gestão e apoio aos usuários.
- Melhorias pontuais diversas de estabilidade e prevenção de bugs.

---

### Versão 1.0.0.9 (17/11/2020)

[TELA PRINCIPAL]

- Melhoria visual na Tela Principal.
- Nova funcionalidade Anotações do Usuário na Tela Principal.

[CADASTRO]

- Inclusão dos Ambientes Organizacionais.
- Exportação da estrutura de Unidades Organizacionais para imagem bitmap (.bmp).
- Inclusão das Unidades Organizacionais no Cadastro de Vínculos.
- Inclusão dos Ambientes Organizacionais e das Unidades Organizacionais na tela Consultas e Posicionamentos.
- Possibilidade de filtragem dos registros por Ambientes ou Unidades Organizacionais na tela Consultas e Posicionamentos.
- Inclusão da sincronização de ocorrências de Afastamentos do SIGEPE (importação de arquivo .xls).

[CARREIRAS]

- Aprimoramento do cabeçalho da tabela na Edição de Portaria (MS Word) na Tela Progressões Funcionais, de modo a mostrar o termo "Posicionamentos" em duas células mescladas acima de "Anterior" e "Atual".
- Possibilidade de filtragem dos registros por Ambientes ou Unidades Organizacionais na tela Progressões Funcionais.

[FERRAMENTAS]

- Em Notificações Eletrônicas, inclusão da possibilidade de salvamento de links conjuntamente com o texto padrão.
- Em Sincronizações Cadastrais, inclusão da sincronização de unidades de lotação, com funcionalidade de correspondências entre as unidades importadas e as Unidades Organizacionais do sistema.

[RELATÓRIOS]

- Novas Listagens adicionadas relativas aos Ambientes Organizacionais e Unidades Organizacionais.

[OUTROS]

- Exportação de dados para MS Excel com formatação aprimorada e pré-configuração de impressão, com cabeçalho e rodapé.
- Melhorias pontuais diversas de estabilidade e prevenção de bugs.
