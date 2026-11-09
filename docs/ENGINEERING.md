# Padrões de Engenharia — HMB Tecnologia

Este documento estabelece **diretrizes recomendadas** para os projetos da organização. Não significa que controles de CI, proteção de branches ou regras de segurança estejam tecnicamente habilitados. Políticas específicas de cada projeto prevalecem.

## 1. Arquitetura e desenvolvimento

- Respeitar os padrões e contratos existentes em cada repositório.
- Manter separação adequada entre regras de negócio, persistência, integrações e interfaces.
- Priorizar mudanças incrementais e compatíveis.
- Documentar decisões arquiteturais e impactos relevantes.
- Evitar refatorações extensas sem justificativa e aprovação.

## 2. Qualidade de código

- Aplicar convenções da linguagem e do projeto.
- Usar análise estática, formatação e revisão quando disponíveis.
- Escrever código claro, com tratamento explícito de erros.
- Manter commits pequenos e descritivos.
- Não introduzir dependências sem avaliar manutenção, segurança e licenciamento.

## 3. Segurança e privacidade

- Não armazenar segredos em código, histórico Git ou logs.
- Validar entradas e aplicar autorização no servidor.
- Usar privilégios mínimos em contas técnicas, pipelines e integrações.
- Proteger dados pessoais e informações confidenciais.
- Comunicar vulnerabilidades de maneira privada conforme [SECURITY.md](../SECURITY.md).

## 4. Dados e integrações

- Utilizar consultas parametrizadas e transações quando apropriado.
- Planejar migrations com validação do ambiente e estratégia de recuperação.
- Considerar concorrência, idempotência e retentativas em operações críticas.
- Versionar contratos de integração quando necessário.
- Não executar mudanças destrutivas sem autorização explícita.

## 5. Testes

- Executar build e verificações aplicáveis antes da revisão.
- Cobrir alterações de regras de negócio com testes proporcionais ao risco.
- Testar cenários de falha, autorização e concorrência em fluxos críticos.
- Registrar limitações e distinguir testes automatizados de validação operacional.
- Não declarar homologação concluída sem evidências verificáveis.

## 6. Git e pull requests

- Utilizar branches dedicadas para mudanças relevantes.
- Descrever objetivo, escopo, riscos, testes e possíveis impactos.
- Solicitar revisões conforme a política do projeto.
- Preservar alterações concorrentes e reconciliar o estado da branch antes de publicar.
- Evitar force pushes em branches compartilhadas e protegidas.

## 7. Implantação e operação

- Confirmar ambiente, versão, dependências e configuração antes do deploy.
- Planejar rollback ou recuperação de mudanças críticas.
- Monitorar falhas, desempenho e disponibilidade.
- Registrar incidentes e correções de forma rastreável.
- Não presumir que sucesso de CI equivale à validação completa do ambiente.

## 8. Precedência

Requisitos contratuais, políticas de segurança aprovadas, documentação específica do projeto e restrições operacionais vigentes têm precedência sobre estas diretrizes gerais.
