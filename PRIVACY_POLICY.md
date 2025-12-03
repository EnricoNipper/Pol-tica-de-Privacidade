# Política de Privacidade - Extensão de Automação de Registro de Tempo

**Última atualização:** 3 de dezembro de 2025

## 1. Introdução

Esta extensão do Google Chrome foi desenvolvida **exclusivamente para uso interno da Pixforce**, com o objetivo de **facilitar tarefas repetitivas dos funcionários** ao automatizar o registro de horas trabalhadas. A extensão consolida dados do TiqueTaque (sistema de ponto eletrônico) e Google Calendar (eventos de reunião) e os envia ao sistema Timesheet Pixforce, eliminando o preenchimento manual diário.

**⚠️ Importante:** Esta é uma ferramenta de uso corporativo interno, destinada apenas aos colaboradores da Pixforce para otimizar processos internos.

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
Os dados são utilizados **exclusivamente para uso interno da empresa** com os seguintes propósitos:
- Facilitar o trabalho diário dos funcionários, eliminando preenchimentos manuais repetitivos
- Consolidar automaticamente registros de ponto e reuniões
- Preencher lacunas com atividade padrão (fallback)
- Enviar registros consolidados ao Timesheet Pixforce

**📌 Nota:** A extensão NÃO compartilha dados com entidades externas. Todo o processamento é feito localmente e os dados são enviados apenas para os sistemas corporativos da Pixforce.

### 3.2 Armazenamento Local
- Todas as configurações são armazenadas localmente no dispositivo via `chrome.storage.local`
- Nenhum dado é enviado a servidores de terceiros além dos sistemas integrados (Google Calendar, TiqueTaque, Timesheet Pixforce)

## 4. Compartilhamento de Dados

### 4.1 Uso Interno - Não Vendemos Dados
**Esta é uma ferramenta corporativa de uso interno.** Declaramos que NÃO:
- Vendemos ou transferimos dados de usuários a terceiros
- Usamos dados para fins não relacionados ao registro de tempo
- Compartilhamos dados para fins de análise de crédito ou empréstimos
- Distribuímos a extensão publicamente (uso restrito aos funcionários da Pixforce)

### 4.2 Sistemas Corporativos Integrados
A extensão se comunica apenas com **sistemas internos da Pixforce e ferramentas corporativas**:
- **Google Calendar API**: Para buscar eventos de reunião (Google Workspace corporativo)
- **API TiqueTaque**: Para buscar registros de ponto eletrônico
- **Timesheet Pixforce**: Para enviar registros consolidados (sistema interno)

**🔒 Segurança:** Todas as comunicações são internas ou com serviços corporativos autorizados pela empresa.

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
