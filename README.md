# 🤖 Spring AI Java — Integração com Modelos de IA (OpenAI)

Projeto backend desenvolvido com **Spring Boot** que demonstra a integração com modelos de Inteligência Artificial utilizando **Spring AI**, permitindo geração de texto, respostas inteligentes e construção de APIs baseadas em LLMs.

O objetivo do projeto é fornecer uma base prática e organizada para uso de IA em aplicações Java modernas.

---

## 🚀 Tecnologias Utilizadas

### 🔙 Backend
- Java 17+  
- Spring Boot  
- Spring AI  
- Maven  
- REST APIs  
- OpenAI API (ou outros provedores compatíveis)  
- Lombok  
- Spring Web  

---

## ⚙️ Como Rodar o Projeto Localmente

### 1️⃣ Clonar o Repositório

```bash
git clone <url-do-repositorio>
cd spring-ai-java-erudio-main
```
2️⃣ Configurar Variáveis de Ambiente

Você precisará de uma chave de API da OpenAI (ou outro provedor suportado).

📌 application.yml ou application.properties

Exemplo:

spring:
  ai:
    openai:
      api-key: SUA_API_KEY_AQUI

Ou via variável de ambiente:

export OPENAI_API_KEY=SUA_API_KEY_AQUI

3️⃣ Build do Projeto
```
mvn clean install
```
4️⃣ Executar a Aplicação
```
mvn spring-boot:run
```
Ou:

java -jar target/*.jar
5️⃣ Acessar a API

Servidor disponível em:

👉 http://localhost:8080

📡 Endpoints Principais
🔹 Gerar Texto com IA
POST /api/ai/generate

Body:

{
  "prompt": "Explique o que é inteligência artificial"
}

Resposta:

{
  "response": "Inteligência artificial é..."
}
🔹 Chat com IA
POST /api/ai/chat

Permite interações mais dinâmicas com contexto.

🧠 Decisões Técnicas

-Spring Boot foi escolhido pela robustez e padrão corporativo.

-Spring AI abstrai a comunicação com modelos de linguagem (LLMs), facilitando integração.

Arquitetura em camadas:

-Controller → Entrada da API

-Service → Regras de negócio

-Config → Integração com IA

Uso de injeção de dependência para desacoplamento.
REST APIs para facilitar integração com frontend ou outros serviços.
Configuração flexível para múltiplos provedores de IA.
---
📦 Funcionalidades Implementadas

-🤖 Geração de texto com IA

-💬 Chat interativo com contexto

-🔌 Integração com OpenAI via Spring AI

-⚙️ Configuração desacoplada por propriedades

-📡 API REST pronta para consumo
---
🏗️ Estrutura do Projeto
```
src/main/java/
├── controller/
├── service/
├── config/
├── model/
└── application.java
```
---
🚀 Deploy
Backend (Render / Railway / AWS)
Subir projeto no GitHub
Criar serviço Java
Configurar:

Build Command

mvn clean install

Start Command

java -jar target/*.jar

Variáveis de ambiente:

OPENAI_API_KEY
---
🔐 Segurança
Nunca exponha sua API Key no código
Utilize variáveis de ambiente
Considere implementar autenticação para endpoints públicos
---
📈 Possíveis Evoluções

🔐 Autenticação com JWT
📊 Logs e monitoramento
🧠 Memória de contexto (chat persistente)
🔄 Integração com banco de dados
📎 Upload e análise de arquivos
🌐 Integração com frontend (React / Next.js)
---
🎯 Objetivo do Projeto

Servir como base prática para:
Aprender Spring AI
Criar APIs inteligentes com Java
Integrar aplicações com LLMs
Evoluir para soluções reais com IA
---
📚 Referências

https://spring.io/projects/spring-ai
https://platform.openai.com/docs
https://docs.spring.io/spring-boot
---
