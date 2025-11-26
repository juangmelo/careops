# Lab 1 – OWASP Juice Shop

Disciplina: Segurança de Aplicações (DevSecOps)  
Professor: Walter Lopes  
Aluno: (Juan Gabriel da Costa Melo)  
Data: (26/11/2025)

---

## 1. Objetivo do Lab

- Explorar uma aplicação propositalmente vulnerável (OWASP Juice Shop).
- Identificar vulnerabilidades relacionadas ao OWASP Top 10 (2025).
- Registrar, para cada vulnerabilidade encontrada:
  - como foi explorada,
  - qual o impacto,
  - qual categoria OWASP,
  - e sugestões iniciais de mitigação.
- Transferir o aprendizado para o sistema CareOps+.

---

## 2. Ambiente Utilizado

- Instância do OWASP Juice Shop:
  - URL: https://expert-zebra-v9qp4qv59xq3pxpx-3000.app.github.dev/user#/search
- Navegador utilizado:
  - Opera
- Ferramentas auxiliares (se usar):
  - (ex.: DevTools, extensões, proxies, etc.)

---

## 3. Vulnerabilidades Encontradas

Preencha uma subseção para cada vulnerabilidade.

### 3.1 Vulnerabilidade #1

- Endpoint / funcionalidade: Criação de uma review de um produto
- Como foi descoberta: Inspecionando o elemento da página o OWASP Juice Shop
- Categoria OWASP: A01
- Payload / passo a passo (resumo, sem expor segredos reais): Criar uma review de um produto qualquer, copiar o mesmo payload que foi utilizado pela aplicação e reutilizar o payload para um produto diferente, podendo alterar o usuario criado ou outras informações
- Impacto (para o negócio / usuários): Usuario malicioso pode se passar por um usuario legitimo e gerar impacto na organização ou terceiros
- Possíveis mitigações: Controle de acesso aplicado tambem no lado do servidor

### 3.2 Vulnerabilidade #2

- Endpoint / funcionalidade: Busca de produtos
- Como foi descoberta: Analisando caixas de texto na aplicação
- Categoria OWASP: A03
- Payload / passo a passo: Inserir payload malicioso no prompt de "search" 
- Impacto: Usuarios legitimos podem ver as alterações causadas por usuarios maliciosos
- Possíveis mitigações: Sanitização dos dados inseridos

### 3.3 Vulnerabilidade #3

- Endpoint / funcionalidade: Diretório FTP da aplicação
- Como foi descoberta: Procurando o robots.txt
- Categoria OWASP: A05
- Payload / passo a passo: No robots.txt, verificar a url que está "escondida" e assim acessar e explorar seu conteúdo
- Impacto: Arquivos da aplicação sensíveis podem ser vistos pelos usuários


## 4. Conexão com o CareOps+

Escolha **pelo menos 2 vulnerabilidades** encontradas no Juice Shop e responda:

### 4.1 Vulnerabilidade A (referência à seção 3.x)

- Vulnerabilidade no Juice Shop:
- Vulnerabilidade semelhante que poderia existir na CareOps+:
- Endpoint da CareOps+ que poderia ter problema parecido:
- Ideia de como mitigar isso na CareOps+:

### 4.2 Vulnerabilidade B

(Mesma estrutura.)

---

## 5. Reflexão Final

Responda em poucas linhas:

- O que mais te surpreendeu ao explorar o Juice Shop?
- Alguma vulnerabilidade parece “boba” de evitar, mas aparece em muitos sistemas reais?
- Que práticas do SDLC seguro (NIST SSDF / OWASP SAMM) ajudariam a evitar esses problemas?
