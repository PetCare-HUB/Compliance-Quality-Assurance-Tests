# PetCare Hub — Compliance, Quality Assurance & Tests

## Objetivo da entrega

Este repositório reúne os artefatos da disciplina **Compliance, Quality Assurance & Tests** para o Challenge FIAP 2026 em parceria com a **CLYVO VET**.

A entrega apresenta a proposta estratégica do **PetCare Hub**, seus critérios de qualidade, riscos, métricas de sucesso, roadmap e a modelagem arquitetural baseada em **TOGAF/ArchiMate**.

## Problema escolhido

A jornada de saúde do pet ainda é fragmentada. Na prática, o responsável costuma procurar a clínica apenas em situações de urgência, vacinação ou sintomas claros. Isso reduz a continuidade do cuidado, dificulta a prevenção, enfraquece o vínculo com a clínica e diminui a recorrência de consultas.

O problema não é exclusivo da CLYVO VET. Ele representa uma dor ampla do mercado veterinário: baixa adesão preventiva, perda de histórico longitudinal e pouca previsibilidade para clínicas e responsáveis.

## Solução proposta

O **PetCare Hub** é uma plataforma de cuidado preventivo e contínuo para pets. A solução conecta app mobile, APIs, sensores IoT, banco Oracle e dashboard clínico para transformar dados do pet em alertas preventivos e indicadores de acompanhamento.

### Componentes principais

- **App Mobile do tutor:** acompanha score de saúde, alertas, calendário preventivo e perfil do pet.
- **API Java:** API principal da solução, responsável pelo domínio operacional, regras de negócio e integração dos dados do pet.
- **API .NET:** API B2B para dashboard de clínicas, focada em leitura, métricas, pets em risco, alertas e histórico clínico.
- **Banco Oracle:** base relacional principal, mantendo histórico longitudinal do pet.
- **IoT:** coleira smart e comedouro/ambiente para coleta de sinais comportamentais, alimentação e condições ambientais.
- **Arquitetura TOGAF/ArchiMate:** visão estratégica, negócio, sistema e tecnologia.

## Diferenciais competitivos

1. **Score de Saúde:** indicador simples para classificar o risco do pet.
2. **Histórico longitudinal:** centralização de dados clínicos, preventivos e comportamentais.
3. **Dashboard B2B:** visão para clínicas acompanharem pets em risco e oportunidades de contato preventivo.
4. **Dados IoT integrados à jornada clínica:** sensores alimentam alertas e métricas.
5. **Modelo preventivo:** a clínica não espera o tutor procurar atendimento; ela atua de forma proativa.

## Benchmarking

| Solução | Foco principal | Limitação em relação ao PetCare Hub |
|---|---|---|
| Petlove | Marketplace e serviços pet | Não é focada em monitoramento clínico contínuo |
| VetSmart | Plataforma veterinária e apoio clínico | Não acompanha a jornada preventiva do tutor de forma contínua |
| Tractive | Rastreamento e wearable pet | Não integra clínica, histórico clínico e dashboard veterinário |
| FitBark | Monitoramento de atividade animal | Foco individual no pet, sem integração clínica robusta |
| Sistemas veterinários tradicionais | Gestão clínica e prontuário | Dependem de interação manual e não coletam dados contínuos |
| PetCare Hub | Continuidade preventiva da jornada veterinária | Integra tutor, clínica, histórico, score e IoT |

## Critérios de qualidade

| Critério | Como será tratado |
|---|---|
| Performance | Latência inferior a 2 segundos para geração e exibição de alertas |
| Segurança | Criptografia na comunicação, controle de acesso e proteção de dados conforme LGPD |
| Usabilidade | Interface simples para tutor e dashboard objetivo para clínicas |
| Disponibilidade | Meta mínima de 99,5% de disponibilidade da plataforma |
| Confiabilidade | Dados rastreáveis e taxa de falsos positivos inferior a 5% |
| Escalabilidade | Separação por APIs e infraestrutura preparada para múltiplas clínicas e pets |

## Riscos e mitigação

| Risco | Impacto | Mitigação |
|---|---|---|
| Baixa adesão dos tutores | Reduz dados e continuidade de uso | Onboarding simples, notificações úteis e acompanhamento da experiência |
| Excesso de notificações | Pode gerar fadiga e desengajamento | Priorização por criticidade e personalização dos alertas |
| Falhas ou inconsistências nos sensores IoT | Pode gerar score incorreto ou falso alerta | Validação por histórico longitudinal e limites aceitáveis |
| Privacidade e segurança dos dados | Risco jurídico e perda de confiança | Criptografia, controle de acesso e boas práticas LGPD |
| Baixa adesão das clínicas | Reduz escalabilidade do modelo B2B | Dashboard simples e foco em recorrência clínica |
| Crescimento do volume de dados | Pode afetar performance e custo | Arquitetura escalável baseada em APIs e nuvem |

## Métricas de sucesso

| KPI | Meta inicial | Fonte |
|---|---|---|
| Retenção de tutores em 90 dias | Superior a 70% | Analytics do aplicativo |
| NPS do tutor | Superior a 75 | Pesquisa de satisfação |
| Adesão preventiva | Aumento de 30% em vacinas e consultas preventivas | Dashboard clínico e registros veterinários |
| Tempo entre alerta crítico e ação clínica | Inferior a 24h | Logs da API e histórico de notificações |
| Recorrência clínica / LTV por pet | Crescimento de 20% | Métricas financeiras e analytics |

## Roadmap

| Sprint | Entregas previstas |
|---|---|
| Sprints 1 e 2 | MVP com app mobile, API Java, banco de dados, protótipo IoT e arquitetura TOGAF |
| Sprint 3 | Integração app + API + sensores, notificações inteligentes, dashboard clínico evoluído e fluxos conversacionais |
| Sprint 4 | IA para priorização de risco, analytics para clínicas e modelo de assinatura B2B |

## Arquitetura TOGAF/ArchiMate

O arquivo `PetCare.archimate` contém a modelagem arquitetural no Archi. O PDF `docs/Modelo_TOGAF_PetCare_Hub.pdf` documenta as etapas A, B, C e D do TOGAF ADM:

- **Etapa A — Architecture Vision:** stakeholders, drivers, assessments, goals, requirements, principles e constraints.
- **Etapa B — Business Architecture:** papéis, serviços, processos, funções, interfaces, eventos e processos AS-IS/TO-BE.
- **Etapa C — Information Systems Architecture:** componentes de aplicação, serviços, objetos de dados e processos de aplicação.
- **Etapa D — Technology Architecture:** nodes, devices, software, network, artifacts e facilities.

## Estrutura do repositório

```txt
.
├── PetCare.archimate
├── README.md
├── integrantes.txt
├── docs/
│   ├── Pitch_PetCare_Hub.pdf
│   ├── Modelo_TOGAF_PetCare_Hub.pdf
│   ├── checklist_qa.md
│   └── links.txt
└── entrega/
    ├── Pitch_PetCare_Hub.pdf
    ├── Modelo_TOGAF_PetCare_Hub.pdf
    └── integrantes.txt
```

## Entrega final solicitada pela disciplina

A pasta `entrega/` contém os três arquivos exigidos:

1. `Pitch_PetCare_Hub.pdf`
2. `Modelo_TOGAF_PetCare_Hub.pdf`
3. `integrantes.txt`

## Equipe

| Integrante | RM |
|---|---|
| Alexander Dennis Isidro Mamani | 565554 |
| Kelson Zhang | 563748 |
