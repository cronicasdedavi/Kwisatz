KWISATZ

DECISIONS.md

Documento: Registro de decisões arquiteturais
Versão: 0.1.0
Status: Em elaboração
Projeto: KWISATZ
Repositório oficial: https://github.com/cronicasdedavi/Kwisatz

---

1. Objetivo

Este documento registra decisões importantes relacionadas à arquitetura, tecnologias, funcionamento e desenvolvimento do KWISATZ.

Cada decisão deverá apresentar seu contexto, justificativa, consequências e estado atual.

O objetivo é preservar o histórico do projeto e evitar mudanças sem análise ou justificativa.

2. Estados das decisões

- Proposta: decisão ainda em avaliação.
- Aceita: decisão aprovada para orientar o projeto.
- Substituída: decisão posteriormente trocada por outra.
- Rejeitada: alternativa analisada e descartada.

Decisões aceitas ainda poderão ser revistas quando novas evidências justificarem uma mudança.

---

3. Decisões arquiteturais

ADR-001: Agente central único

Status: Aceita

Decisão:

O KWISATZ utilizará um único agente central responsável por coordenar módulos internos especializados.

Justificativa:

Essa organização busca manter uma direção centralizada, preservar o contexto e evitar que agentes independentes disputem o controle do sistema.

Consequências:

- O núcleo central coordenará as atividades.
- Os módulos terão responsabilidades específicas.
- Novas capacidades poderão ser incorporadas modularmente.

ADR-002: Evolução autônoma como capacidade central

Status: Aceita

Decisão:

A evolução autônoma será uma característica transversal da arquitetura, não apenas uma ferramenta isolada.

Justificativa:

O KWISATZ deverá melhorar continuamente seu funcionamento, conhecimentos, estratégias e capacidades técnicas.

Consequências:

O sistema deverá possuir mecanismos para:

- Avaliar o próprio desempenho.
- Aprender com experiências.
- Identificar limitações.
- Pesquisar melhorias.
- Desenvolver novas ferramentas.
- Modificar componentes próprios.
- Testar alterações.
- Comparar resultados.
- Reverter mudanças problemáticas.

O autoaperfeiçoamento técnico deverá ocorrer com isolamento, testes e controles de segurança.

ADR-003: Arquitetura modular

Status: Aceita

Decisão:

O sistema será organizado em módulos internos com responsabilidades bem definidas.

Justificativa:

A modularidade facilitará manutenção, testes, expansão e evolução.

Consequências:

- Cada módulo deverá possuir interfaces definidas.
- Alterações deverão minimizar dependências desnecessárias.
- Novas funcionalidades poderão ser incorporadas progressivamente.

ADR-004: Execução híbrida

Status: Aceita

Decisão:

O KWISATZ deverá combinar recursos locais e serviços em nuvem.

Justificativa:

Essa organização permitirá aproveitar recursos computacionais diferentes e oferecer acesso por computador e celular.

Consequências:

- Componentes poderão executar localmente ou remotamente.
- A comunicação deverá ser segura.
- O sistema deverá lidar com desconexões.
- A distribuição definitiva dependerá de testes de viabilidade.

ADR-005: Python para o núcleo

Status: Aceita como escolha inicial

Decisão:

Python será a linguagem principal do núcleo central.

Justificativa:

Sua disponibilidade de bibliotecas para inteligência artificial, automação, integração e desenvolvimento facilita a construção do sistema.

Consequências:

O núcleo e seus módulos principais serão inicialmente desenvolvidos em Python.

ADR-006: TypeScript, React e Next.js para a interface

Status: Aceita como escolha inicial

Decisão:

A interface utilizará TypeScript, React e Next.js, com possibilidade de funcionamento como PWA.

Justificativa:

Essa combinação permite desenvolver uma interface web adaptável a computadores e celulares.

Consequências:

A interface será separada do núcleo e se comunicará com ele por meio de uma API.

ADR-007: FastAPI para comunicação

Status: Aceita como escolha inicial

Decisão:

FastAPI será utilizado para disponibilizar a API do sistema.

Justificativa:

Permite integrar componentes Python com interfaces externas e oferecer comunicação HTTP e WebSocket.

ADR-008: PostgreSQL para persistência

Status: Aceita como escolha inicial

Decisão:

PostgreSQL será o banco de dados principal inicialmente planejado.

Justificativa:

Oferece persistência estruturada e suporte a diferentes necessidades de armazenamento.

Consequências:

A memória persistente será construída sobre uma infraestrutura de banco de dados confiável.

ADR-009: pgvector para busca vetorial

Status: Proposta aceita para avaliação

Decisão:

pgvector será considerado para recuperação de informações por similaridade semântica.

Justificativa:

Poderá ampliar a capacidade de recuperação contextual da memória.

Consequências:

A adoção definitiva dependerá de testes que demonstrem sua utilidade e eficiência.

ADR-010: Ollama para modelos locais

Status: Aceita como opção inicial

Decisão:

Ollama será considerado uma das ferramentas para executar modelos de inteligência artificial localmente.

Justificativa:

Permite experimentar modelos locais e reduzir dependência de serviços externos.

Consequências:

A utilização dependerá da capacidade computacional disponível e do desempenho dos modelos.

ADR-011: Playwright para navegação

Status: Aceita como escolha inicial

Decisão:

Playwright será utilizado como tecnologia inicial para automação de navegador.

Justificativa:

Permite automatizar interações com páginas e aplicações web.

Consequências:

As operações deverão respeitar permissões, segurança e limitações dos serviços utilizados.

ADR-012: GitHub como fonte oficial da verdade

Status: Aceita

Decisão:

O repositório GitHub será a fonte oficial da verdade do KWISATZ.

Justificativa:

O projeto precisa manter código, documentação, decisões, histórico e testes organizados em um local central.

Consequências:

- Alterações importantes deverão ser versionadas.
- A documentação oficial deverá permanecer no repositório.
- O histórico de mudanças deverá ser preservado.
- O estado do projeto deverá ser conferido com base no repositório.

ADR-013: Prioridade para soluções gratuitas

Status: Aceita

Decisão:

O projeto priorizará ferramentas, modelos e infraestrutura gratuitos.

Justificativa:

O objetivo é construir o KWISATZ sem depender de despesas recorrentes.

Consequências:

- Alternativas gratuitas deverão ser avaliadas primeiro.
- Limitações dos planos gratuitos deverão ser consideradas.
- Recursos pagos não poderão ser tratados como garantidos.
- A viabilidade de funcionamento contínuo deverá ser testada.

ADR-014: Desenvolvimento incremental

Status: Aceita

Decisão:

O KWISATZ será desenvolvido por etapas, com testes e validação progressiva.

Justificativa:

Construir todo o sistema simultaneamente aumentaria a complexidade e dificultaria a identificação de falhas.

Consequências:

- A fundação será construída antes das funcionalidades avançadas.
- Cada etapa deverá ser testada.
- Problemas deverão ser corrigidos antes de avançar.
- A documentação deverá acompanhar o desenvolvimento.

ADR-015: Segurança e controle de autonomia

Status: Aceita

Decisão:

A autonomia do KWISATZ deverá coexistir com controles de segurança e permissões.

Justificativa:

Um sistema capaz de executar tarefas e modificar seus próprios componentes precisa preservar a integridade e a estabilidade.

Consequências:

- Operações sensíveis terão controles específicos.
- Alterações técnicas deverão ser testadas.
- O sistema deverá manter mecanismos de recuperação.
- Ações de maior impacto poderão exigir aprovação.

---

4. Revisão das decisões

As decisões deverão ser revisadas quando:

- Novas tecnologias apresentarem vantagens relevantes.
- Testes demonstrarem problemas na escolha atual.
- Os requisitos do projeto mudarem.
- A infraestrutura disponível mudar.
- Uma decisão comprometer desempenho, segurança ou confiabilidade.

Uma decisão substituída deverá permanecer registrada no histórico.

5. Estado do documento

- [x] Estrutura de registro definida.
- [x] Decisões arquiteturais iniciais documentadas.
- [ ] Revisão e aprovação do documento.
- [ ] Validação técnica das escolhas.
- [ ] Atualização conforme o desenvolvimento.

6. Observações finais

Este documento representa o registro inicial das decisões do KWISATZ.

As escolhas tecnológicas classificadas como iniciais ainda deverão passar por validação prática.

O histórico de decisões deverá ser mantido durante toda a evolução do projeto.

O GitHub será a fonte oficial da verdade do KWISATZ.