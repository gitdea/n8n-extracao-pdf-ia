# Automação com IA: Extração de Dados de PDF (n8n)

Fluxo em **n8n** que automatiza a extração de dados pessoais de documentos PDF,incluindo **digitalizados/escaneados**,usando **OCR + LLM**, com interface conversacional via chat.

## Como funciona

1. **Chat Trigger** recebe o PDF enviado pelo usuário no chat
2. **Extração de texto** identifica se o PDF é digital (texto direto) ou escaneado
3. **OCR (Mistral)** quando não há texto extraível, aplica OCR no documento digitalizado
4. **AI Agent (Groq LLM)** estrutura os dados em JSON: nome, CPF, endereço e telefone
5. **Data Table** salva os registros em base consultável
6. **Agente Consultor** responde perguntas em linguagem natural sobre os dados extraídos

## Stack

- **n8n** orquestração do fluxo
- **Groq (LLM)** extração e estruturação dos dados
- **Mistral OCR** leitura de PDFs digitalizados/escaneados
- **n8n Data Tables** armazenamento dos registros

## Como usar

1. No n8n, vá em **Workflows → Import**
2. Selecione o arquivo JSON deste repositório
3. Configure suas credenciais (Groq API e Mistral API)
4. Ative o workflow e use o chat para enviar PDFs

## Observações

- Este é um **ambiente de demonstração** os dados nos exemplos (CPF, nomes etc.) são **todos fictícios**.
- O fluxo está **pronto para produção**: basta conectar credenciais corporativas e um banco de dados real (PostgreSQL, MySQL etc.).

## Autora

**Andrea Cruz Leonardo** Desenvolvedora Back-End | Automação com n8n e IA


