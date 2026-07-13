#  Base de Conhecimento Inteligente: Protocolo STIR/SHAKEN no Brasil

##  Contexto e Objetivos do Projeto
Este repositório foi desenvolvido como entrega para o desafio prático da plataforma **DIO**. O objetivo principal é centralizar a curadoria de dados técnicos e regulatórios sobre o protocolo **STIR/SHAKEN** (comercialmente chamado no Brasil de **"Origem Verificada"** pela Anatel). 

Esta base de dados estruturada alimenta o **Google NotebookLM**, criando uma Inteligência Artificial especializada e imune a alucinações para responder dúvidas complexas de engenharia de telecomunicações.

---

## Fontes Utilizadas para o Treinamento da IA
As fontes abaixo foram salvas, documentadas e injetadas no ecossistema do NotebookLM:
* **Resolução nº 777 da Anatel**: Regulamentação oficial do sistema "Origem Verificada" no Brasil.
* **Manuais Técnicos da ABR Telecom**: Infraestrutura de gerenciamento de chaves criptográficas públicas e privadas.
* **Documentação RFC do IETF**: Padrões globais dos cabeçalhos SIP Identity e especificações de tokens PASSport (JWT).

---

## Engenharia de Prompts e "Cicatrizes" de Desenvolvimento

### Prompts de Validação Aplicados no NotebookLM:
1. **Tentativa Inicial (Fraca):** *"O que é STIR/SHAKEN?"* -> *Resultado:* Resposta genérica focada nas diretrizes americanas da FCC.
2. **Tentativa Avançada (Sucesso):** *"Com base exclusivamente nos documentos da Anatel anexados, explique como o protocolo STIR/SHAKEN altera os cabeçalhos de sinalização SIP para exibir a marca da empresa em redes VoLTE?"* -> *Resultado:* Resposta altamente técnica e precisa alinhada ao cenário brasileiro.

###  (Problemas e Soluções):
* **Problema:** A IA misturou legislações antigas de spam com as regras novas de validação de ID de chamadas.
* **Solução:** Filtragem de fontes no GitHub. Removemos artigos informativos e mantivemos o texto consolidado bruto da resolução da Anatel, instruindo o prompt a ignorar dados fora desse escopo.

---

## Testes de Validação da IA (Prontos para Reuso)
Copie e cole estas perguntas no chat do NotebookLM para auditar o conhecimento da IA:

* **Pergunta 1:** *"Considerando a topologia do STIR/SHAKEN, qual é a diferença técnica e operacional no tratamento de uma chamada que recebe uma atribuição 'Attestation Class A' em comparação com uma 'Attestation Class C'?"*
* **Pergunta 2:** *"Se um fraudador interceptar a chamada na Rede de Trânsito e alterar o número de telefone de origem para aplicar Spoofing, como o servidor STI-VS da operadora de destino detectará essa quebra de segurança?"*
