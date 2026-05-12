---
layout: default
title: Política de Privacidade — Ellie
description: Como o app Ellie trata dados pessoais.
---

# Política de Privacidade — Ellie

**Última atualização:** 12 de maio de 2026

Esta política descreve como o aplicativo **Ellie** (referido aqui como "o app") trata dados pessoais. O app é desenvolvido por **Davydso Malvarenga** (referido aqui como "nós").

Ao usar o app, você concorda com os termos descritos abaixo. Se não concordar, não use o app e desinstale-o.

---

## 1. Quem somos

- **Responsável:** Davydso Malvarenga
- **Contato:** davydsomalvarenga@gmail.com
- **Aplicativo:** Ellie — assistente de organização pessoal e profissional para Android.

---

## 2. Que dados coletamos

### 2.1 Dados de identificação anônima

Quando você abre o app pela primeira vez, criamos uma **identificação anônima** automática via Firebase Authentication (sign-in anônimo). Essa identificação:

- É um identificador aleatório (UID) gerado pela Google.
- **Não está vinculada ao seu nome, e-mail, telefone ou conta Google.**
- É usada apenas para controlar o limite gratuito de uso diário.
- Não permite, por si só, identificar você como pessoa.

### 2.2 Contador de uso

Mantemos no nosso servidor (Cloud Firestore) um contador diário de quantas vezes você usou a interpretação por IA naquele dia. Esse contador:

- É associado à sua identificação anônima.
- Reseta automaticamente todo dia em UTC.
- Existe apenas para impedir abuso e respeitar o limite gratuito (10 leituras/dia).

### 2.3 Conteúdo enviado para processamento

Quando você usa "Capturar" (texto, áudio, foto, receita médica), o conteúdo é **enviado para o Google Gemini (Gemini Developer API)** para que a inteligência artificial interprete e extraia eventos, tarefas e rotinas. Esse envio:

- Acontece apenas no momento do uso, sob seu comando explícito.
- O conteúdo (texto/áudio/imagem) **não é armazenado** pelos nossos servidores nem pelos da Google após o processamento, conforme política de dados do Gemini Developer API.
- A resposta interpretada volta direto pro app e é guardada **apenas no seu aparelho**.

### 2.4 Dados que ficam só no seu aparelho

Os compromissos, tarefas e rotinas que você confirma após a interpretação ficam armazenados **localmente no banco de dados do seu aparelho** (SQLite). **Nada disso é enviado pra nuvem nem é acessível por nós.** Se você desinstalar o app, esses dados são apagados.

---

## 3. O que NÃO coletamos

- **Nome, e-mail, telefone ou qualquer dado de identificação pessoal direta.**
- **Localização geográfica.**
- **Contatos da agenda do telefone.**
- **Histórico de navegação, dados de outros apps, ou métricas comportamentais.**
- **Áudios, fotos ou textos persistidos** — só passam pela IA no momento do uso.

---

## 4. Permissões do sistema

O app pede as seguintes permissões. Cada uma tem propósito específico:

| Permissão | Uso |
|---|---|
| **Microfone** | Apenas durante a gravação manual de áudio para captura. |
| **Câmera** | Apenas quando você escolhe "tirar foto" pra capturar uma receita ou imagem. |
| **Galeria / Mídia** | Quando você escolhe "selecionar áudio" ou "selecionar imagem" da sua galeria. |
| **Notificações** | Para entregar lembretes de eventos, tarefas e rotinas. |
| **Alarmes exatos** | Para que lembretes disparem no horário certo, sem agrupamento. |
| **Ignorar otimização de bateria** | Recomendado em alguns fabricantes para que lembretes não atrasem em segundo plano. |

Nenhuma dessas permissões é usada em segundo plano, exceto as notificações agendadas (alarmes locais).

---

## 5. Compartilhamento com terceiros

Dependemos de **quatro serviços da Google** para que o app funcione:

1. **Google Gemini (Gemini Developer API)** — processa o conteúdo enviado para interpretação. [Política de privacidade do Google.](https://policies.google.com/privacy)
2. **Firebase Authentication (sign-in anônimo)** — cria e mantém sua identificação anônima.
3. **Cloud Firestore** — mantém o contador diário de uso.
4. **Firebase Crashlytics** — recebe relatórios automáticos quando o app trava. Conteúdo dos relatórios:
   - Pilha de chamadas (*stack trace*) do erro
   - Modelo do aparelho, versão do Android e versão do app
   - Identificação anônima (mesmo UID do item 2)
   - **Nenhum conteúdo seu** (texto/áudio/foto/agenda) é enviado.

   Você pode desligar relatórios de erro em **Configurações > Privacidade > Enviar relatórios de erro** a qualquer momento.

Esses serviços são fornecidos pela Google e regidos pela política de privacidade da Google. **Não compartilhamos seus dados com nenhum outro terceiro** (publicidade, analytics comportamental, etc).

Não usamos:
- Google Analytics
- Facebook SDK
- Qualquer rede de ads
- Qualquer ferramenta de tracking comportamental ou perfilamento publicitário

---

## 6. Inteligência artificial e conteúdo médico

O app usa **IA generativa (Google Gemini)** para interpretar o conteúdo que você compartilha. Isso significa:

- A interpretação **pode conter erros**. Sempre revise o que foi extraído antes de confirmar.
- Para **receitas médicas**, o app pode extrair medicamentos, doses e horários como referência para lembretes. **O app não substitui orientação médica, farmacêutica ou de profissional de saúde.** Em caso de dúvida sobre dose, frequência ou tratamento, consulte o profissional que prescreveu.
- Não usamos a IA para fornecer aconselhamento médico, diagnóstico ou recomendações de tratamento.

---

## 7. Seus direitos (LGPD, GDPR)

Mesmo coletando apenas identificação anônima, você tem direito a:

- **Acessar** os dados associados à sua identificação anônima — entre em contato e enviaremos o contador atual.
- **Apagar** os dados — desinstale o app (limpa o aparelho) e/ou entre em contato pedindo a exclusão dos dados no Firestore.
- **Solicitar esclarecimentos** sobre o tratamento.

**Como exercer:** envie e-mail para **davydsomalvarenga@gmail.com** com o assunto "Privacidade Ellie".

Como não há identificação direta, talvez precisemos da identificação anônima (UID) gerada pelo Firebase no seu aparelho — você consegue extrair via console do desenvolvedor ou pedindo suporte.

---

## 8. Crianças

O app não é direcionado a crianças menores de 13 anos. Não coletamos intencionalmente dados de menores. Se você é responsável e identificou uso por um menor, entre em contato.

---

## 9. Segurança

- A comunicação com o Gemini Developer API e Firebase usa **HTTPS / TLS**.
- A identificação anônima é validada pelo **Firebase App Check** (Play Integrity), impedindo que outros aplicativos clonem credenciais.
- Dados locais são protegidos pela sandbox padrão do Android.

Apesar dos cuidados, nenhum sistema é 100% seguro. Use o app por sua conta e risco.

---

## 10. Mudanças nesta política

Podemos atualizar esta política. Mudanças relevantes serão comunicadas via descrição da loja e/ou nesta página. A data de "Última atualização" no topo indica quando o documento foi modificado.

---

## 11. Contato

- **E-mail:** davydsomalvarenga@gmail.com

---

*Este documento foi escrito para o lançamento inicial do app. Está sujeito a melhorias conforme o app evolui.*
