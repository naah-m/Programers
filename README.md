# Programers

## 👥 Integrantes do Grupo
Nathália Mantovani | DEV
Alexis Rondo | HOM 
Vinicius Rodrigues de Oliveira | PRD

## 📝 Descrição da Solução (Desenvolvimento de um app para Vans Escolares)
O aplicativo é voltado para empresas e/ou motoristas de vans escolares de todo o território brasileiro, sendo um checklist onde tanto o motorista/supervisor do veículo quanto os pais e/ou responsáveis terão acesso. Ambas as partes poderão guiar-se por meio de notificações, por exemplo, "O motorista está chegando, prepare-se para embarcar!", além de notificar ao motorista quando algum aluno não for utilizar de seus serviços, visando facilitar a mobilidade e recálculo da rota do mesmo. Para o recálculo da rota, o app teria a integração de um mapa direcional sendo possível realizar rotas melhores, seguras e mais eficientes para buscar e deixar os alunos colocados à sua responsabilidade.
Com um checklist de recebimento de alunos pelo motorista e de entrega aos responsáveis, todo o processo fica registrado com hora e data, trazendo um melhor controle sobre a localização de cada aluno, e existindo uma maior prevenção a possíveis acidentes, como o esquecimento de crianças e/ou adolescentes dentro dos veículos e até mesmo dentro das escolas. Outros complementos ainda podem ser atribuídos como: Cada aluno ter uma espécie de carteira de identificação, contendo observações importantes sobre tipo sanguíneo, enfermidades, necessidades especiais, uso de medicações, dentre outros.

## 🎯 Objetivo
Aplicativo voltado a motoristas de vans escolares e responsáveis legais de crianças e/ou adolescentes, com checklist operacional, notificações (ex.: “O motorista está chegando”) e roteirização inteligente para recalcular rotas conforme faltas/ausências dos alunos notificadas pelos responsáveis. O sistema registra a entrega/recebimento de alunos com data e hora, aumentando a segurança e a rastreabilidade. Cada aluno possui perfil de identificação (tipo sanguíneo, necessidades especiais, observações médicas).

## 🧭 Método Adotado
- Metodologia ágil (Scrum): O grupo organiza o trabalho em etapas curtas (sprints), definindo tarefas claras, revisando o que foi feito e ajustando sempre que necessário para manter o ritmo e a qualidade do projeto;
- Ciclo DevOps com GitHub: Todo o código é versionado no GitHub, permitindo colaboração entre os integrantes, histórico de mudanças e integração contínua das entregas;
- Prototipagem rápida com Figma e testes no Azure: Antes de programar, criamos protótipos no Figma para validar a ideia das telas. Depois, usamos o Azure para rodar testes práticos e simular o ambiente de produção.

## 💡 Proposta de Valor
Segurança e tranquilidade para famílias e escolas (trilha auditável de cada etapa);
Economia de tempo/combustível com rotas otimizadas e confirmação de presença;
Simplicidade trazendo fluxos claros (check-in/out, ausências, notificações push) e UX para motoristas;
Confiabilidade mantendo registros com carimbo de data/hora e confirmação por responsável.

## 👤 Clientes
Motoristas/empresas de vans escolares (gestão de rotas, alunos e comunicação);
Responsáveis legais de alunos (acompanhar chegada/saída, ausências, histórico); 
(Opcional) Escolas para integração com controle de portaria/chamada.

## 🧩 Segmento de Clientes
B2B: frotas de transporte escolar terceirizadas;
B2C: motoristas autônomos que atendem um conjunto de famílias;
Institucional (opcional): escolas particulares que queiram integração com portaria.

## ⚙️ Etapas e Recursos de Implantação
Levantamento de ideias → entender necessidades de motoristas e pais;
Protótipo inicial → criar telas simples mostrando o fluxo;
Construção do sistema → programar backend e app;
Testes → verificar se as funções principais funcionam;
Implantação → liberar versão de teste e ajustar com feedback.

## 🧱 Rascunho da Solução
App Mobile (RN/Expo): Motorista e responsável (perfis distintos), consumo da API, push notifications, mapa com rota e paradas;
API Quarkus: Autenticação (JWT), gestão de usuários/alunos/veículos, eventos (check-in/out), ausências, cálculo de rota (chama serviço externo), auditoria;
Banco de Dados: PostgreSQL (relacional) com chaves e logs de auditoria;
Integrações: FCM (push), Mapbox/Google API Directions e/ou Geocoding, (opcional) webhook para escola.

Use Case do projeto:
1- Responsável marca “ausência” do aluno para o dia;
2- API recalcula rota (chamada Directions API) e atualiza paradas;
3- Motorista inicia rota e faz checklist (itens do veículo e lista de alunos);
4- Ao aproximar-se da parada, app dispara push: “Motorista está chegando”;
5- Motorista registra check-in do aluno com horário; no desembarque, check-out;
6- Todos os eventos ficam disponíveis no histórico do responsável.

## 🔑 Recursos-Chave
Linguagens/Frameworks: Java (Quarkus), TypeScript (React Native/Expo);
Infra: Docker, Railway/Render/Azure;
APIs: Mapbox/Google (directions/geocoding) e Firebase Cloud Messaging;
Controle de Versão: GitHub;
Qualidade: Testes manuais e automáticos;
Segurança: Login por perfis, criptografia de senhas, HTTPS.

## 🎥 Vídeo Explicativo
A ser upado

## 💻 Código-Fonte do MVP
Ainda não há código fonte

## 🗄️ Banco de Dados
Modelo (tabelas principais):
- usuários
- alunos
- veículos
- rotas
- paradas
- eventos
- checklists

## 🧮 Versões dos Softwares
- Java 21, Quarkus 3.x
- Node.js 20.x, Expo SDK 51+, React Native 0.74+
- Oracle Database Express Edition 21c
- Oracle SQL Developer 23.x
- Docker 26+, GitHub Actions

## 🚀 Próximos Passos
- Testar com grupo pequeno de motoristas e responsáveis;
- Adicionar notificações automáticas ao se aproximar da parada;
- Melhorar relatórios de uso (tempo de rota, atrasos, ausências);
- Possibilidade de integração com app Waze;
- Fortalecer segurança dos dados.

## 📚 Referências
Links e fontes utilizadas como base para o desenvolvimento:

Projeto de Lei que propõe sensores e alarmes para evitar que crianças sejam esquecidas em vans escolares. Poderia ser complementado com o app
https://www.camara.leg.br/noticias/1036347-projeto-torna-obrigatorio-sensor-e-alarme-para-alertar-sobre-crianca-esquecida-em-van-escolar

Possibilidade de integração do Waze com o app
https://support.google.com/waze/partners/answer/7422931?hl=pt-BR&ref_topic=7422416&sjid=17480164701825637122-SA


