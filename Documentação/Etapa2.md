# 2. Plano de Inteligência Competitiva (IC)

## 2.1 Identificação das Necessidades de IC
Foram identificadas as seguintes principais decisões estratégicas dentro do contexto analisado:  
- Quais tratamentos priorizar (mais rentáveis ou mais demandados);
- Como aumentar a taxa de retorno de pacientes;
- Gestão de agenda (reduzir horários ociosos);
- Investimento em marketing (quais serviços divulgar);
- Como aumentar a lucratividade do consultório.  
Após análise, definimos que o KIT (Key important topic) a ser priorizado como principal estratégia de negócio a ser trabalhada será “Como aumentar a lucratividade do consultório”.  
E dentre as principais questões a serem levantadas, podendo categorizá-las como KIQs (Key Intelligence Questions) separamos as consideradas mais importantes para o negócio e seu desenvolvimento competitivo, sendo:  
- Quais são os tratamentos mais realizados?
- Quais tratamentos geram maior receita?
- Qual o custo médio por tipo de tratamento?
- Qual a margem de lucro por procedimento?
- Qual o perfil dos pacientes por tipo de tratamento?
- Qual a taxa de retorno dos pacientes?
- Quais tratamentos têm maior taxa de cancelamento ou abandono?
As Key Intelligence Questions são de extrema importância para o desenvolvimento das empresas nos dias atuais, e no contexto do presente trabalho é necessário nos atentarmos a cada uma delas, tais como saber quais os tratamentos mais realizados para identificar quais serviços devem ser priorizados, tanto pela demanda quanto pelo faturamento. Ainda, saber o custo médio dos tickets e atendimentos para definir se os preços estão competitivos e ainda assim lucrativos; definir o perfil do cliente é importante para adotar medidas de marketing específicas para um público alvo mais bem definido. Além disso, analisar a taxa de retorno dos pacientes é de suma importância para acompanhamento, para que possam ser explorados os pontos fortes para a fidelização do cliente. Por fim, saber quais tratamentos têm a maior taxa de cancelamento ou abandono contribui para a busca de um padrão que faz com que o atendimento não seja concluído, de modo que esse padrão possa ser corrigido. 

## 2.2 Mapeamento de Dados e Necessidades de Informação
Dentre as Informações necessárias, podem ser listados os seguintes dados, que após analisados se transformarão em informação a ser utilizada para adquirir as respostas dos KIQs:  
|KIQ (Key Intelligence Question)|Informação Necessária|
| :--- | :--- |
|Quais são os tratamentos mais realizados?|- Quantidade de Clientes - Tratamento Feito|
|Quais tratamentos geram maior receita?|- Quantidade de Clientes - Faturamento - Tratamento Feito|
|Qual o custo médio por tipo de tratamento?|- Quantidade de Clientes - Tratamento Feito - Custo dos Materiais - Hora do Profissional - Faturamento|
|Qual a margem de lucro por procedimento?|- Faturamento por Procedimento - Custo dos Materiais - Hora do Profissional|
|Qual o perfil dos pacientes por tipo de tratamento?|- Quantidade de Clientes - Idade - Sexo|
|Qual a taxa de retorno dos pacientes?|- Quantidade de Clientes - Intervalo entre consultas - Data|
|Quais tratamentos têm a maior taxa de cancelamento ou abandono?|- Quantidade de Clientes - Quantidade de Cancelamento - Tratamento Feito|  

Isto posto, as fontes de dados internas já existentes para atender às questões são:  
- Planilha de pacientes
- Planilha de pagamentos
- Histórico manual de tratamentos  

Atualmente, são utilizados principalmente os seguintes dados dos pacientes: nome, data de nascimento, endereço, telefone, procedimento/tratamento realizado, dente tratado, valor do procedimento, observações.  
Porém, é perceptível que os dados atuais possuem baixa confiabilidade e difícil análise. Como principal problema pode-se mencionar o fato de os dados não serem estruturados, havendo a necessidade clara de um sistema centralizado. 

## 2.3 Especificação de Requisitos Informacionais
Conforme mapeado como necessidade para alcançar a decisão-chave para o negócio, foram levantados os seguintes requisitos para o sistema:  
- Cadastro completo de pacientes
- Histórico de tratamentos por paciente
- Registro de pagamentos (status, forma, valor)
- Controle de agenda
- Classificação de tratamentos  

De modo a apoiar a decisão-chave do negócio, foram definidos os seguintes KPIs, com o objetivo de mensurar o desempenho do consultório e subsidiar a tomada de decisões estratégicas para conseguir aumentar a lucratividade:  
- Receita por tratamento
- Lucro por tratamento
- Ticket médio por paciente
- Taxa de retorno de pacientes
- Taxa de cancelamento
- Ocupação da agenda  

Nesse contexto, visando construir uma solução que possibilite o negócio obter e gerir melhor os dados de modo que seja possível sua posterior análise para embasar tomadas de decisão, foram definidos os seguintes requisitos funcionais e informacionais:   
- Cadastro de pacientes
- Gerenciamento de tratamentos
- Gerenciamento financeiro
- Gerenciamento de Agenda
- Dashboard com dados de pagamento
- Dashboard com dados de tratamentos realizados
- Gerenciamento de frequência de pacientes.  

A definição dos KPIs propostos é fundamental para apoiar a tomada de decisões estratégicas no consultório, uma vez que permite transformar dados operacionais em indicadores claros de desempenho e rentabilidade.  
A receita por tratamento possibilita identificar quais procedimentos geram maior faturamento, enquanto o lucro por tratamento aprofunda essa análise ao considerar os custos envolvidos, permitindo avaliar efetivamente a rentabilidade de cada serviço ofertado. Já o ticket médio por paciente contribui para a compreensão do valor gerado por atendimento, auxiliando na definição de estratégias de precificação e oferta de serviços complementares.  
A taxa de retorno de pacientes é um indicador essencial para mensurar a fidelização, evidenciando a capacidade do consultório em manter relacionamentos de longo prazo com seus clientes. Em contrapartida, a taxa de cancelamento permite identificar falhas operacionais ou insatisfações, possibilitando ações corretivas para redução de perdas e melhoria da experiência do paciente.  
Por fim, a ocupação da agenda está diretamente relacionada à eficiência operacional, permitindo avaliar o aproveitamento do tempo disponível dos profissionais e identificar oportunidades de otimização.  
Em conjunto, esses indicadores fornecem uma visão abrangente do desempenho do consultório, permitindo não apenas entender o que gera maior retorno financeiro, mas também melhorar a retenção de pacientes e otimizar o uso dos recursos disponíveis.  

## 2.4 Levantamento de Fontes de Dados Existentes
Atualmente, a única fonte de dados disponível é uma planilha em Excel, utilizada como ficha cadastral dos pacientes. Nessa planilha, encontram-se registrados dados pessoais, como nome, endereço, telefone e a origem da indicação. Além disso, o documento contempla informações relacionadas aos procedimentos realizados, incluindo as respectivas datas, os dentes tratados, os valores dos tratamentos, a quantidade de parcelas e os valores correspondentes a cada parcela.  
A partir da planilha, conseguimos obter uma grande parcela dos dados que necessitamos para o funcionamento da solução que será construída, entretanto ainda será necessário coletar alguns dados como custos dos materiais utilizados em cada procedimento, cancelamentos de pacientes, valor da hora do profissional e se o pagamento do procedimento foi efetuado.

## 2.5 Compliance de TI e Segurança da Informação
Estabelecimentos de saúde no Brasil, incluindo consultórios odontológicos, estão sujeitos a normas que regulam coleta, armazenamento, acesso e proteção dos dados dos pacientes, que são classificados como dados sensíveis pela legislação vigente.  
As leis e normas aplicáveis a este contexto são as seguintes:  
- **LGPD (Lei nº 13.709/2018)**: disciplina o tratamento de dados pessoais e sensíveis; exige base legal (consentimento, tutela da saúde, contrato), formalização por escrito, aviso de privacidade e medidas técnicas de segurança.
- **Resolução CFO nº 91/2009**: autoriza a digitalização de prontuários e estabelece prazo mínimo de 20 anos de guarda a partir do último registro.
- **Lei nº 13.787/2018**: regulamenta prontuários digitais, exigindo integridade, autenticidade, confidencialidade e uso de certificado digital ICP-Brasil.
- **Código de Ética Odontológica (Res. CFO nº 118/2012)**: impõe sigilo profissional, atualização dos prontuários e resguardo da privacidade do paciente.  

Ainda, é possível listar algumas diretrizes que segurança da informação que regem os estabelecimentos de saúde brasileiros.  
- **Controle de acesso**: somente profissionais autorizados podem consultar ou editar registros, com uso de criptografia e nomeação de encarregado de dados (DPO).
- **Backups automáticos e periódicos**: substituição obrigatória do modelo de cópias manuais esporádicas.
- **Política de retenção**: manutenção dos prontuários por no mínimo 20 anos; descontinuações devem ser documentadas.
- **Consentimento formalizado**: termo escrito com linguagem clara, especificando finalidade, direitos do paciente e bases legais do tratamento.
- **Monitoramento contínuo**: verificações periódicas das práticas de tratamento, controle de acessos e prazos de retenção.

Em conclusão, o consultório encontra-se em situação de não conformidade, uma vez que o armazenamento em planilhas locais realizado sem controle de acesso, sem backup regular e sem formalização do consentimento contraria a LGPD, a Res. CFO nº 91/2009, a Lei nº 13.787/2018 e o Código de Ética Odontológica. O descumprimento expõe o profissional a sanções administrativas da Agência Nacional de Proteção de Dados (ANPD), ações judiciais e danos reputacionais. A adequação é, portanto, uma obrigação legal urgente.