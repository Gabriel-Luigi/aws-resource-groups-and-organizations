# Grupos de Recursos e Organizações na AWS

Simulação de governança de recursos AWS para uma empresa com múltiplos departamentos, utilizando Resource Groups, Organizations e Cost Budgets.

[Read in English](README.md)

## Objetivo

Demonstrar uma configuração prática de governança na AWS, aplicando tagueamento de recursos, hierarquia organizacional e controle de custos - conceitos frequentemente exigidos em vagas de Cloud e FinOps.

## Ambiente

- Amazon AWS Resource Groups & Tag Editor
- Amazon AWS Organizations
- Amazon AWS Billing and Cost Management

## Estrutura de Governança

```
Root
├── LandingZones
│   ├── Corp
│   └── Online
├── Platform
└── Sandbox
```

## Configuração Principal

- Resource Group: `rg-cloud-fundamentals-lab`, tag `project = cloud-fundamentals-lab`
- Unidades Organizacionais (OUs) criadas no AWS Organizations para representar a separação entre departamentos
- Orçamento mensal de custo: limite de US$ 1,00, com alertas em 85% e 100%

## Evidências

### 1. Criação do Resource Group com chave e valor de tag
![Resource Group](images/Resource-Group-Details.png)

### 2. Criação da estrutura de Organização
![Organization](images/Organizational-structure.png)

### 3. Orçamento mensal com alertas (85% e 100%)
![Budget](images/Budget.png)
![Alerts](images/Budget-Alerts.png)

## Observações

- Este projeto simula uma estrutura simplificada de governança via AWS Organizations (Platform, LandingZones com Corp/Online, e Sandbox) para uma empresa hipotética com múltiplos departamentos.
- Como esta conta AWS possui apenas um membro, a movimentação de contas entre as OUs não foi testada - a hierarquia de OUs demonstra o padrão de design de governança, e não uma implantação completa multi-conta.
- O orçamento mensal foi configurado como medida de segurança de FinOps antes da criação de qualquer recurso tarifável.
