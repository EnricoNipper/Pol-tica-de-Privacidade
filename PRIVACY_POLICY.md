# Política de Privacidade - Extensão de Automação de Registro de Tempo

**Última atualização:** 3 de dezembro de 2025

## 1. Introdução

Esta extensão do Google Chrome ("Automação de Registro de Tempo") foi desenvolvida para automatizar o registro de horas trabalhadas, consolidando dados do TiqueTaque (sistema de ponto eletrônico) e Google Calendar (eventos de reunião) e enviando-os ao sistema Timesheet Pixforce.

## 2. Dados Coletados

### 2.1 Informações de Autenticação
- **Token OAuth do Google**: Utilizado exclusivamente para acessar eventos do Google Calendar do usuário
- **Token do Timesheet Pixforce**: Obtido via cookies do sistema para enviar registros de tempo
- **ID do funcionário TiqueTaque**: Necessário para buscar registros de ponto

### 2.2 Dados Processados
- **Eventos do Google Calendar**: Títulos de reuniões, horários de início/fim, localização e número de participantes
- **Registros de Ponto (TiqueTaque)**: Horários de entrada e saída registrados no sistema de ponto
- **Configurações do usuário**: Projeto padrão, atividade fallback e observações personalizadas

## 3. Como Usamos os Dados

### 3.1 Propósito Único
Os dados são utilizados **exclusivamente** para:
- Consolidar automaticamente registros de ponto e reuniões
- Preencher lacunas com atividade padrão (fallback)
- Enviar registros consolidados ao Timesheet Pixforce

### 3.2 Armazenamento Local
- Todas as configurações são armazenadas localmente no dispositivo via `chrome.storage.local`
- Nenhum dado é enviado a servidores de terceiros além dos sistemas integrados (Google Calendar, TiqueTaque, Timesheet Pixforce)

## 4. Compartilhamento de Dados

### 4.1 Não Vendemos Dados
**Declaramos que NÃO:**
- Vendemos ou transferimos dados de usuários a terceiros
- Usamos dados para fins não relacionados ao registro de tempo
- Compartilhamos dados para fins de análise de crédito ou empréstimos

### 4.2 APIs de Terceiros
A extensão se comunica apenas com:
- **Google Calendar API**: Para buscar eventos de reunião
- **API TiqueTaque**: Para buscar registros de ponto
- **Timesheet Pixforce**: Para enviar registros consolidados

## 5. Segurança

- Tokens de autenticação são armazenados de forma segura via `chrome.identity` e `chrome.storage`
- Comunicação com APIs usa HTTPS (criptografia TLS)
- Nenhum dado sensível é registrado em logs públicos

## 6. Permissões Necessárias

### 6.1 Justificativa de Permissões
- **`identity`**: Autenticação OAuth com Google Calendar
- **`storage`**: Armazenar configurações localmente
- **`cookies`**: Acessar token do Timesheet Pixforce
- **`tabs`**: Detectar autenticação no Timesheet
- **Host permissions**: Comunicação com APIs (Calendar, TiqueTaque, Timesheet)

## 7. Controle do Usuário

### 7.1 Remoção de Dados
- Desinstalar a extensão remove automaticamente todos os dados armazenados localmente
- Revogar acesso ao Google Calendar em https://myaccount.google.com/permissions

### 7.2 Transparência
- Todo o código-fonte está disponível para auditoria
- Nenhum código remoto é executado (sem `eval()`, scripts externos)

## 8. Conformidade com LGPD/GDPR

- Coletamos apenas dados essenciais para o funcionamento da extensão
- Usuário tem controle total sobre seus dados
- Dados não são retidos após desinstalação

## 9. Alterações nesta Política

Notificaremos usuários sobre mudanças significativas via atualização da extensão.

## 10. Contato

Para dúvidas sobre privacidade:
- **Email**: [suporte.ai@pixforce.com]
- **Empresa**: Pixforce 
- **Website**: https://www.pixforcemaps.com

---

**Versão da Extensão:** 1.1  
**Manifesto Version:** 3  
**Publicado em:** Chrome Web Store
