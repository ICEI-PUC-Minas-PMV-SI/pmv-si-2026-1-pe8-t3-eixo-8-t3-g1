# 3. Desenvolvimento de alternativas de soluções de SI
No presente projeto, será desenvolvida uma solução de sistema de informação baseada em uma aplicação web apoiada por um banco de dados relacional. O sistema em questão apoiará o consultório na tomada de decisões relevantes para atender às necessidades estratégicas levantadas anteriormente, principalmente as relacionadas à gestão de agenda, priorização de tratamentos, controle de taxa de retorno e aumento da lucratividade do serviço. Para o cenário atual, construir uma solução de sistema web se mostra mais adequada à resolução dos problemas do consultório porque não existe um sistema centralizado de controle e armazenamento das informações, sendo inviável a extração e organização dos dados existentes para a criação de um BI.  
Na aplicação, serão inicialmente desenvolvidas funcionalidades relacionadas ao cadastro de pacientes e gestão de agenda. Será desenvolvida uma página dedicada ao registro das informações principais dos pacientes, conforme já utilizado nas planilhas atuais, de modo à facilitar a adaptação dos usuários ao novo sistema. Assim, no cadastro será possível preencher os seguintes campos: nome completo; telefone principal e complementar; endereço; origem (indicação, captação, entre outros); data de cadastro; data de nascimento. Como acréscimo ao que já existe no cadastro atual, será implementado um campo de preenchimento livre onde será descrito um histórico do paciente, quais tratamentos e procedimentos relevantes ele já fez em outros consultórios e outras informações que o dentista acreditar serem relevantes para a ficha, que servirá como um prontuário de consulta. Um outro campo de informações relevantes de saúde também será criado, podendo ser indicado, por exemplo, se o paciente é diabético, hipertenso, entre outros dados médicos.  
Dentro da página de informações do paciente, será dedicada uma seção para os orçamentos realizados, indicando a data, qual procedimento orçado e para quais dentes, valor informado. Outra seção será dedicada ao controle de atendimento realizados, informando o valor total do tratamento, as especificações do procedimento realizado, datas e formas de pagamentos, indicação de quitado ou a receber. Posteriormente, será implementada uma seção dedicada a um odontograma integrado onde o dentista poderá indicar quais dentes foram ou serão objeto de tratamento.  
Já no que diz respeito à gestão de agenda, será desenvolvida uma página dedicada à agenda de atendimentos, com visão diária e mensal. A agenda será integrada com a página de cadastro dos clientes, sendo possível acessar os dados do cliente ao clicar em seu nome indicado na agenda, somente sendo possível agendar um paciente quando ele já tiver seu respectivo cadastro. Para o registro de novos atendimentos, será preenchido qual o paciente, objetivo do atendimento e tempo reservado, sendo possível inserir observações pertinentes. Por fim, existirá um campo de lista para indicar se o paciente compareceu, faltou ou remarcou a consulta.   
A partir dessas funcionalidades iniciais, será possível acessar e extrair relatórios do sistema que indiquem: quais procedimentos são mais realizados no consultório; qual o valor do ticket médio dos serviços fornecidos; quais pacientes possuem maior índice de ausência ou reagendamento; valores recebidos e em aberto; qual a principal origem dos pacientes; quais pacientes estão inadimplentes; quais pacientes não retornaram ao consultório nos últimos 3 meses.  
Assim, conclui-se que a adoção de um sistema de informação baseado em uma aplicação web com banco de dados relacional apresenta-se como a solução primordial e mais adequada para o cenário atual do consultório, precedendo a implementação isolada de ferramentas puramente focadas em business intelligence. Essa escolha justifica-se pela atual descentralização e desestruturação dos dados gerados pelo estabelecimento, que hoje encontram-se fragmentados em planilhas locais, o que inviabiliza a extração íntegra e confiável das informações para análises avançadas. Dessa forma, o sistema atua resolvendo a raiz do problema operacional, uma vez que ao unificar o cadastro de pacientes, o fluxo de caixa e a gestão de agenda em uma plataforma única, o sistema elimina o retrabalho e mitiga o risco de perda de informações sensíveis. Simultaneamente, essa nova arquitetura relacional garante a coleta padronizada dos dados do dia a dia, gerando uma base de dados limpa e robusta.  
Por fim, a viabilidade do sistema deve ser analisada sob o ponto de vista técnico e financeiro. No ponto de vista técnico, a aplicação será desenvolvida tendo como base a linguagem de programação TypeScript, CSS e HTML para estruturação e estilização da interface. No frontend, será utilizado o framework React, ao passo que o backend se baseia em Node.js e Express. O banco de dados será construído em SQL Server através da plataforma Microsoft Azure, utilizando inicialmente os créditos estudantis disponíveis para o desenvolvimento. As tecnologias utilizadas são compatíveis com as necessidades do sistema, contribuindo para um desenvolvimento robusto e estável, além de estarem correspondentes aos conhecimentos técnicos da equipe de desenvolvimento e o tempo necessário para a entrega.   
Já sob o aspecto financeiro, a aplicação apresentará baixo custo para o consultório, sendo necessário adquirir uma licença Microsoft Azure de aproximadamente cinquenta reais mensais. A hospedagem será feita em plataformas gratuitas tanto do frontend quanto do backend, eliminando este custo de manutenção. Por ser construída com base em linguagens de fácil acesso, a aplicação terá fácil manutenção. Assim, tendo em vista as vantagens oferecidas ao consultório ao implementar um sistema robusto e unificado para centralizar seus processos, o custo principal de se manter uma licença Microsoft Azure oferece um equilíbrio financeiro vantajoso para o empreendimento.  

## 3.1 Conexão com o Plano de IC e Planejamento da Solução
O desenvolvimento do sistema foi projetado para atuar como a principal ferramenta de suporte ao KIT definido para o negócio: "Como aumentar a lucratividade do consultório". Para que esse objetivo seja alcançado, o sistema centraliza e estrutura os processos operacionais diários, transformando-os em dados analisáveis.    
Abaixo, demonstra-se como as funcionalidades da aplicação resolvem as lacunas de informação e respondem diretamente às KIQs mapeadas:    
|KIQ|Processo resolvido pelo sistema|
| :--- | :--- |
|KIQ 01: Quais são os tratamentos mais realizados?|Através da seção de controle de atendimentos dentro da ficha do paciente, o dentista registra as especificações de cada procedimento realizado. De acordo com a lista de procedimentos registrados, será possível exibir um relatório exibindo o quantitativo de cada um deles.|
|KIQ 02: Quais tratamentos geram maior receita?|A integração entre o registro de tratamentos e o Módulo Financeiro permitirá que o sistema associe os serviços executados aos valores cobrados por eles, exibindo as receitas correspondentes.|
|KIQ 03 e KIQ 04: Qual o custo médio por tipo de tratamento e qual a margem de lucro por procedimento?|O sistema armazenará o valor cobrado do cliente em cada atendimento na aba financeira. Ao inserir os dados complementares de custos de materiais e do valor da hora do profissional, a aplicação terá a base de cálculo necessária para que o administrador extraia relatórios de rentabilidade e margem de lucro real por serviço.|
|KIQ 05: Qual o perfil dos pacientes por tipo de tratamento?|O módulo centralizado de Cadastro de Pacientes exigirá o preenchimento uniforme de dados pessoais e o cruzamento desses dados com o histórico de tratamentos de cada paciente fornecerá os dados sobre qual público consome quais tratamentos.|
|KIQ 06: Qual a taxa de retorno dos pacientes?|A funcionalidade de Agenda, integrada ao cadastro, mapeará o histórico contínuo de marcações. A aplicação calculará os intervalos entre as consultas e gerará um alerta no relatório identificando, por exemplo, os pacientes que não retornaram ao consultório nos últimos 3 meses.|
|KIQ 07: Quais tratamentos têm maior taxa de cancelamento ou abandono?|O campo de status na nova agenda digital e o status de orçamentos permitirá identificar quais tratamentos possuem maior desmarcação e quais não são efetivados após o orçamento.|

O desenvolvimento inicial do sistema priorizará a implementação das funcionalidades de cadastro de pacientes e gestão de agenda, módulos estruturais que se integram diretamente ao controle financeiro. A aplicação contará com uma página de registro centralizado contendo informações pessoais, contatos, histórico clínico detalhado e o controle de orçamentos e procedimentos executados por paciente. De forma conectada, a plataforma oferecerá uma agenda interativa com visão diária e mensal, permitindo o agendamento atrelado aos cadastros existentes e a rápida atualização do status das consultas para organizar a rotina do consultório. A partir desses módulos, será desenvolvida a página de relatórios onde será possível extrair os relatórios definidos como prioritários através do plano de inteligência competitiva.  
Assim, é possível construir o seguinte quadro-resumo:  

|Problema mapeado|Solução proposta|Como será resolvido no sistema|
| :--- | :--- | :--- |
|Descentralização das informações|Migrar os dados de planilhas locais dispersas para uma aplicação web centralizada, suportada por um banco de dados relacional com armazenamento estruturado em nuvem|Infraestrutura centralizada na nuvem e Banco de Dados Relacional|
|Ausência de controle financeiro|Desenvolver um módulo para mapear receitas, vinculando os tratamentos executados aos valores efetivamente recebidos, inadimplências e formas de pagamento|Funcionalidade de Gerenciamento Financeiro (Aba Financeiro / Registro de Entradas e Pagamentos)|
|Controle precário de agenda|Estruturar uma agenda digital centralizada e integrada, capaz de organizar os horários de atendimento de forma visual e controlar o fluxo e comparecimento dos pacientes|Funcionalidade de Gerenciamento de Agenda (Visão interativa mensal/diária e alteração de status de presença)|
|Cadastro não uniforme de pacientes|Padronizar a coleta de informações por meio de formulários digitais com campos estruturados obrigatórios para dados pessoais, contatos, origem e características de saúde|Funcionalidade de Cadastro de Pacientes (CRUD com campos padronizados)|
|Inexistência de relatórios estratégicos|Extrair e processar os dados operacionais da rotina da clínica para gerar painéis analíticos com base nos KPIs estabelecidos|Funcionalidade de Geração de Relatórios pelo administrador|
|Falta de acompanhamento do histórico do cliente|Unificar a jornada do paciente em um prontuário digital único, consolidando orçamentos fornecidos, evolução clínica e histórico de consultas passadas e futuras |Funcionalidade de Histórico Clínico e de Orçamentos (Visão detalhada na página do Paciente)|

## 3.2 Levantamento de Requisitos e Modelagem Inicial
Para construir as histórias de usuários, é necessário centrar-se nos três principais atores que utilizarão o sistema: a assistente (ASB), a dentista associada e o dentista titular, que atua como administrador. Assim, tem-se cinco principais histórias de usuários:  

|História de Usuário|Tema|Descrição|
| :--- | :--- | :--- |
|HU01|Gestão de Agenda|Como assistente (ASB), eu quero agendar, alterar e marcar o status de comparecimento das consultas, organizar o fluxo de pacientes de forma eficiente, para otimizar os processos da empresa e gerir de maneira mais organizada.|
|HU02|Prontuário de Tratamentos|Como cirurgiã-dentista, eu quero acessar o histórico de tratamentos realizados pelo paciente, para que eu tenha um registro seguro, rastreável e com respaldo clínico.|
|HU03|Controle de Orçamentos|Como cirurgiã-dentista, eu quero registrar propostas de orçamentos detalhados para que eu possa ter um controle sobre os valores de maior adesão.|
|HU04|Controle Financeiro|Como dentista titular e administrador do sistema, eu quero registrar os pagamentos recebidos e visualizar os saldos pendentes ou em atraso, para que eu tenha controle sobre a inadimplência e saiba a receita total gerada.|
|HU05|Inteligência e Relatórios|Como dentista titular e administrador do sistema, eu quero gerar relatórios pertinentes para que eu consiga tomar decisões estratégicas baseadas em dados visando o aumento da lucratividade do meu consultório.|

Assim como as histórias de usuários, o diagrama de caso de uso também é centrado nos três principais atores do sistema, levando-se ainda em consideração que o usuário administrador realiza todas as atividades também realizadas pelo usuário cirurgião dentista.  
![Diagrama de Caso de Uso](/Documentação/Imagens/casodeuso.png)  

Foram definidos seis requisitos funcionais e quatro requisitos não funcionais para o sistema a ser construído, os quais seguem dispostos nas tabelas a seguir.  

|Requisito Funcional|Descrição|Prioridade|
| :--- | :--- | :--- |
|RF01|O sistema deve possuir um módulo de cadastro completo de pacientes, com dados pessoais, de contatos e informações médicas|Alta|
|RF02|O sistema deve oferecer uma agenda interativa que permita registrar consultas para pacientes cadastrados|Alta|
|RF03|O sistema deve permitir o registro de tratamentos e orçamentos, vinculando-os ao paciente|Alta|
|RF04|O sistema deve disponibilizar um odontograma digital integrado ao prontuário|Baixa|
|RF05|O sistema deve possuir um módulo financeiro para registrar entradas, classificar os status de pagamento e calcular a receita total|Alta|
|RF06|O sistema deve gerar relatórios a partir dos dados do banco associados aos KPIs|Alta|

|Requisito Não Funcional|Descrição|Prioridade|
| :--- | :--- | :--- |
|RNF01|O sistema deve estar em conformidade com a LGPD, garantindo o resguardo e o sigilo dos dados sensíveis|Alta|
|RNF02|O sistema deve possuir controle de acesso autenticado através de login e senha para restringir visualizações sensíveis|Alta|
|RNF03|O sistema deve ser uma aplicação web sustentada por um banco de dados relacional e armazenamento estruturado em nuvem|Alta|
|RNF04|O sistema deve realizar rotinas de backups automáticos e periódicos na nuvem|Média|  

A partir dos requisitos e funcionalidades definidas, o diagrama de entidade e relacionamento do banco de dados a ser construído é o seguinte:  
![Diagrama de Entidade Relacionamento](/Documentação/Imagens/diagramaer.png) 

Isto posto, as ferramentas e plataformas escolhidas para a construção do sistema são:  
- Front-end: React 18 com TypeScript
- Back-end: Node.js com Express
- Banco de dados: SQL Server no Azure SQL Database
- Deploy: Vercel

## 3.3 Protótipo e Planejamento da Arquitetura
O protótipo inicial do sistema apresenta a visão estimada das páginas de pacientes, agenda e financeiro.  
A estrutura de navegação do sistema pode ser representada no fluxo de telas abaixo:  
![Representação do Fluxo de Telas](/Documentação/Imagens/fluxo.png)   

 Assim, a visão inicial do sistema será da página de login, exibida a seguir:  
 ![Tela de login](/Documentação/Imagens/login.png)  

 A partir do login, o usuário acessa a página de Pacientes, onde será possível pesquisar e selecionar um paciente específico para visualizar os dados completos.  
 ![Tela de Paciente1](/Documentação/Imagens/Paciente1.png)   
![Tela de Paciente2](/Documentação/Imagens/Paciente2.png)   

A página de agenda exibirá a visão ampla mensal e o recorte diário lateralmente.  
![Tela de Agenda](/Documentação/Imagens/Agenda.png)  

Por fim, a página de financeiro exibirá os valores já recebidos, pendentes e atrasados com base nas entradas registradas pelo usuário. Esta aba somente poderá ser acessada pelo usuário administrador e pelo dentista associado, não pelo usuário de recepção.  
![Tela de Financeiro](/Documentação/Imagens/Financeiro.png) 

Posteriormente, será implementada a página de relatórios, somente acessível ao usuário administrador, que contará com uma lista de possíveis relatórios a serem apresentados.  
![Tela de Relatórios](/Documentação/Imagens/Relatorios.png) 

## 3.4 Preparação do Desenvolvimento
De acordo com as prioridades levantadas anteriormente, o desenvolvimento do sistema será iniciado pelas páginas de cadastro de pacientes e registro de agenda, páginas que se integram também ao registro financeiro. A partir do desenvolvimento da estrutura front-end dessas páginas, será iniciada a estruturação do banco de dados relacional e da estrutura back-end, o que permitirá a construção, então, dos relatórios estruturados e o funcionamento completo do sistema.  
O projeto será desenvolvido colaborativamente através de um repositório no GitHub, acessível por todos os membros da equipe.  

## 3.5 Geração de Relatórios ou Dashboards Internos
A página de relatórios foi desenvolvida com o objetivo de fornecer aos dentistas e gestores do consultório uma visão estratégica sobre os dados registrados no sistema, permitindo a análise de informações relevantes para apoiar a tomada de decisões. Por meio da centralização e organização dos dados, os relatórios possibilitam identificar padrões de atendimento, desempenho financeiro e comportamento dos pacientes, contribuindo para uma gestão mais eficiente e orientada por dados.  
Os relatórios foram estruturados para responder questões estratégicas importantes para o funcionamento do consultório. Entre elas, destaca-se a identificação dos tratamentos mais realizados, permitindo compreender quais procedimentos possuem maior demanda e auxiliando no planejamento operacional e na alocação de recursos.  
![Relatório1](/Documentação/Imagens/Relatorio1.png)   

Além disso, o sistema possibilita analisar quais tratamentos geram maior receita, oferecendo suporte para decisões relacionadas à investimentos, campanhas e definição de prioridades comerciais.  
![Relatório2](/Documentação/Imagens/Relatorio2.png)     

Outra funcionalidade importante da página de relatórios é a análise de custos médios e margem de lucro por procedimento. Essas informações permitem avaliar a viabilidade financeira de cada tratamento oferecido, auxiliando na precificação dos serviços e no controle financeiro do consultório.  
![Relatório3](/Documentação/Imagens/Relatorio3.png)  

Também é possível identificar o perfil dos pacientes por tipo de tratamento, possibilitando compreender características do público atendido e desenvolver estratégias de atendimento mais personalizadas.  
![Relatório4](/Documentação/Imagens/Relatorio4.png)  

A plataforma ainda fornece indicadores relacionados ao relacionamento e fidelização dos pacientes, como a taxa de retorno ao consultório e os tratamentos com maior índice de cancelamento ou abandono. Essas análises permitem identificar possíveis problemas nos processos de atendimento, satisfação dos pacientes ou eficiência dos tratamentos, contribuindo para a criação de ações de melhoria contínua.  
![Relatório5](/Documentação/Imagens/Relatorio5.png)   
![Relatório6](/Documentação/Imagens/Relatorio6.png)   

Dessa forma, a página de relatórios atua como uma ferramenta de apoio gerencial, transformando dados operacionais em informações estratégicas que auxiliam os profissionais do consultório na tomada de decisões mais assertivas, aumentando a eficiência administrativa, financeira e operacional da clínica.  