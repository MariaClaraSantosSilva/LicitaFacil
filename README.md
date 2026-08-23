# 🏛️ Licita Fácil — Sistema de Gestão de Licitações Públicas

> Sistema desktop para automação e gestão transparente do ciclo de vida de licitações públicas em municípios de pequeno porte, desenvolvido conforme as diretrizes da **Lei Federal nº 14.133/2021**.

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![UI](https://img.shields.io/badge/Interface-Java%20Swing-blue?style=for-the-badge)
![Conformidade Legal](https://img.shields.io/badge/Lei-14.133%2F2021-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen?style=for-the-badge)

---

## 📌 Visão Geral do Projeto

Muitas prefeituras de pequeno porte ainda gerenciam seus processos licitatórios de forma manual (pastas físicas e planilhas soltas), enfrentando problemas como perda de documentos, prazos descontrolados, falta de infraestrutura de TI dedicada e dificuldade na auditoria de processos.

O **Licita Fácil** foi desenvolvido para resolver esse gargalo: um sistema **100% offline**, sem necessidade de banco de dados relacional ou servidor dedicado, garantindo conformidade legal, rastreabilidade total e custo zero de infraestrutura.

Este projeto foi criado como trabalho final da disciplina de **Programação II (2026.1)** no curso de Sistemas de Informação da **Universidade de Pernambuco (UPE)**.

---

## 🚀 Funcionalidades Principais

- **📝 Gestão de Editais:** Criação, inclusão de itens, publicação, cancelamento com justificativa e controle do ciclo de vida via **máquina de estados**, além de exportação em `.txt`.
- **🏢 Cadastro de Fornecedores:** Registro por CNPJ, verificação de habilitação e busca rápida.
- **📊 Propostas & Julgamento:** Suporte a propostas de **Preço** e **Técnica**, com julgamento e adjudicação automática (menor preço, melhor técnica ou técnica e preço).
- **📄 Gestão de Contratos:** Geração automática pós-adjudicação e acompanhamento de status do contrato.
- **🛡️ Auditoria & Rastreabilidade:** Registro detalhado de cada ação (usuário, operação, data e hora) para garantir transparência pública.
- **📈 Relatórios Gerenciais & Dashboard:** Indicadores em tempo real de processos por status, fornecedores mais contratados e economia gerada aos cofres públicos.
- **❓ Central de Ajuda:** Documentação e manual do usuário integrados diretamente na aplicação.

---

## 📐 Arquitetura & Conceitos de POO

A aplicação foi estruturada em uma arquitetura em camadas (**Layered Architecture**) para separar a interface gráfica, as regras de negócio e o modelo de domínio:

```text
├── ui/         -> Interface gráfica (Java Swing / formulários e telas)
├── service/    -> Camada de serviços e regras de negócio
├── model/      -> Entidades do domínio (classes de modelo)
└── enums/      -> Enums transversais para status, modalidades e categorias
