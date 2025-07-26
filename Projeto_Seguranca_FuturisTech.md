# Projeto de Segurança para Aplicações Web e APIs – FuturisTech

**Aluno:** Michele Pereira Martins  
**Módulo:** Desenvolvimento Seguro de Aplicações

---

## Introdução
A FuturisTech é uma empresa moderna e preocupada com a segurança digital. Como está crescendo e lidando com dados importantes, ela precisa garantir que só pessoas autorizadas acessem seus sistemas.

Este projeto apresenta uma proposta prática e segura para controlar quem entra e o que cada pessoa pode fazer dentro dos aplicativos e APIs da empresa, protegendo os dados e garantindo conformidade com boas práticas.

---

## 1. Objetivos do Projeto
- Garantir a segurança no acesso às aplicações e APIs.
- Controlar quem pode acessar o quê, de forma simples e eficaz.
- Cumprir com a Lei Geral de Proteção de Dados (LGPD).
- Documentar e treinar os usuários para uso seguro dos sistemas.

---

## 2. Autenticação e Autorização
Usaremos:
- **Login único (SSO)**
- **Verificação em dois passos (MFA)**
- **Login com conta externa**

Controle de acesso:
- **RBAC** (por papel)
- **ABAC** (por atributos)

---

## 3. Tecnologias e Protocolos Utilizados
- **Servidor de autenticação:** Keycloak ou Auth0
- **Protocolos de segurança:**
  - OAuth 2.0 e OpenID Connect
  - SAML 2.0
- **Criptografia:**
  - Senhas com bcrypt
  - Comunicação com SSL/TLS

---

## 4. Segurança das APIs
- Uso de API Gateway
- Autenticação com token JWT
- Limite de requisições por usuário
- Versionamento de APIs

---

## 5. Medidas Adicionais de Segurança
- Monitoramento por geolocalização
- Logs de acesso e atividades
- Revogação de tokens suspeitos

---

## 6. Conformidade com a LGPD
- Aviso e consentimento de cookies
- Política de privacidade clara
- Painel de preferências de privacidade

---

## 7. Avaliação de Riscos (Modelo STRIDE)

| Componente              | Ameaça (STRIDE)        | Vulnerabilidade                            | Mitigação                                  |
|------------------------|------------------------|--------------------------------------------|---------------------------------------------|
| Usuário                | Spoofing               | Login sem MFA                              | Implementar MFA e bloqueio por tentativas   |
| Sistema de Autenticação| Tampering / Spoofing   | Manipulação de credenciais                 | SSL/TLS, bcrypt, timeout                    |
| Tokens JWT             | Tampering / Disclosure | Token alterado ou com dados sensíveis      | Assinatura digital, evitar dados sensíveis  |
| Sistema de Autorização | Elevation of Privilege | Acesso indevido por falhas de regra        | RBAC/ABAC auditado                          |
| API Gateway            | DoS / Spoofing         | Ataques por requisições em massa           | Rate limiting, verificação de token         |
| APIs                   | Injection / Disclosure | Falta de validação, dados expostos         | Sanitização, autenticação e controle de acesso |

---

## 8. Plano de Resposta a Incidentes
1. **Identificação** – Detectar comportamentos anômalos
2. **Isolamento** – Revogar tokens e bloquear acessos
3. **Correção** – Corrigir falhas e aplicar medidas
4. **Comunicação** – Informar responsáveis e, se necessário, a ANPD
5. **Aprendizado** – Documentar e atualizar políticas

---

## 9. Auditoria e Revisão Contínua
- Auditorias regulares
- Análise dos logs
- Revisão das permissões e regras

---

## 10. Integração com DevSecOps
- Segurança desde o desenvolvimento
- Ferramentas para análise de código seguro

---

## 11. Documentação e Treinamento
- Manual técnico e wiki interna
- Diagramas da arquitetura
- Treinamento para funcionários

---

## Conclusão
Este projeto mostra que é possível proteger os sistemas da FuturisTech com medidas práticas e bem aplicadas. A inclusão do modelo de ameaças ajuda tanto arquitetos quanto gestores a tomar decisões mais conscientes. Segurança digital é um compromisso contínuo.

https://1drv.ms/u/c/3b92918e3ed4f49e/EaL759VjJSZLmyo_CHvnKmkBbX1KkYT6SKLT9Mq2-KnLrQ?e=0zVwF7
