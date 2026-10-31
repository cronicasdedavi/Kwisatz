
# KWISATZ
## Documento central do projeto

**Status:** Planejamento  
**Versão:** 0.1.0  
**Repositório oficial:** https://github.com/cronicasdedavi/Kwisatz

---

## 1. Visão geral

KWISATZ é um projeto de agente pessoal de inteligência artificial, concebido para atuar como um sistema central capaz de compreender objetivos, planejar tarefas, utilizar ferramentas, executar operações autorizadas, aprender com o contexto disponível e manter memória persistente.

O projeto busca construir um agente único, autônomo, adaptável e evolutivo, organizado internamente em módulos especializados.

O KWISATZ não deve ser apenas uma interface de conversa. Sua finalidade é funcionar como um sistema capaz de transformar objetivos em ações, acompanhar sua execução e verificar os resultados.

## 2. Objetivos principais

- Manter um agente central responsável pela coordenação das capacidades do sistema.
- Possuir memória persistente e recuperação contextual.
- Planejar tarefas e acompanhar sua execução.
- Pesquisar informações e avaliar a confiabilidade das fontes.
- Interagir com navegadores, aplicativos e arquivos.
- Criar, modificar e validar artefatos.
- Executar tarefas localmente e utilizar recursos em nuvem quando disponíveis.
- Ser acessível por computador e celular.
- Permitir a substituição e combinação de modelos de IA.
- Evoluir de maneira incremental, sem depender de uma arquitetura rígida.

## 3. Princípios fundamentais

### 3.1 Agente central

O sistema terá um único agente central responsável pelo controle, planejamento e coordenação.

Os módulos internos serão capacidades subordinadas ao agente central, não agentes independentes disputando o controle.

### 3.2 Autonomia com controle

O KWISATZ deverá conseguir planejar e executar tarefas dentro das permissões concedidas.

Operações sensíveis deverão exigir aprovação apropriada.

### 3.3 Adaptabilidade

A arquitetura deverá permitir substituir modelos, ferramentas e componentes sem reconstruir todo o sistema.

### 3.4 Memória persistente

O sistema deverá preservar informações relevantes entre sessões e permitir recuperar o contexto necessário para suas tarefas.

### 3.5 Confiabilidade

A execução deverá considerar checkpoints, recuperação de falhas, validação dos resultados e registro de operações.

### 3.6 Execução híbrida

O projeto deverá combinar recursos em nuvem e recursos locais, permitindo que o computador execute operações que não sejam adequadas à infraestrutura remota.

### 3.7 Custo zero como prioridade

A prioridade é utilizar ferramentas, modelos e infraestrutura gratuitos.

Nenhuma funcionalidade deverá depender de uma promessa não verificada de hospedagem gratuita contínua, processamento ilimitado ou disponibilidade permanente.

## 4. Arquitetura planejada

A arquitetura inicial prevê:

- **Núcleo:** Python.
- **API:** FastAPI.
- **Interface:** TypeScript, Next.js e React.
- **Acesso móvel:** interface adaptável e PWA.
- **Comunicação:** HTTP e WebSocket.
- **Memória:** PostgreSQL, com possibilidade de pgvector em etapa posterior.
- **Modelos:** adaptadores flexíveis, incluindo suporte ao Ollama.
- **Automação de navegador:** Playwright.
- **Execução:** infraestrutura híbrida, com coordenação em nuvem e componente local.

Essas tecnologias representam o planejamento inicial. Sua adoção definitiva dependerá de validação técnica e de custo.

## 5. Segurança e confiabilidade

O KWISATZ deverá incorporar:

- Controle de permissões.
- Isolamento de operações.
- Proteção de credenciais e segredos.
- Auditoria de atividades.
- Aprovação de operações sensíveis.
- Checkpoints e recuperação de execução.
- Verificação dos resultados produzidos.

A autonomia não deverá significar acesso irrestrito ao computador, às contas ou aos dados do usuário.

## 6. Estratégia de desenvolvimento

O desenvolvimento seguirá estas diretrizes:

1. Documentar antes de implementar.
2. Dividir o projeto em etapas pequenas e verificáveis.
3. Validar cada componente antes de avançar.
4. Manter testes para funcionalidades implementadas.
5. Evitar complexidade prematura.
6. Registrar decisões técnicas e suas justificativas.
7. Manter o GitHub como fonte oficial da verdade do projeto.

## 7. Escopo dos requisitos

O planejamento anterior registrou 92 requisitos integrados ao projeto.

A lista integral deverá ser reconstruída, organizada, revisada e validada antes de ser considerada a especificação oficial.

Nenhum requisito deverá ser tratado como confirmado apenas por suposição.

## 8. Estado atual

- [x] Conta GitHub criada.
- [x] Repositório privado criado.
- [x] Branch principal `main` criada.
- [x] README inicial criado.
- [x] `.gitignore` configurado para Python e ferramentas web.
- [ ] Documentação oficial concluída.
- [ ] Arquitetura técnica validada.
- [ ] Requisitos revisados.
- [ ] Ambiente de desenvolvimento preparado.
- [ ] Primeira implementação iniciada.

## 9. Critério de conclusão deste documento

Este documento estabelece a visão geral e os princípios do KWISATZ.

Alterações futuras deverão ser registradas no GitHub e refletidas nos documentos técnicos correspondentes.
