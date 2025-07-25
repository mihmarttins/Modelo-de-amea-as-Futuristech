# 🔐 Modelo de Ameaças – FuturisTech

Este repositório contém o modelo de ameaças da empresa fictícia **FuturisTech**, criado como parte do módulo **Desenvolvimento Seguro de Aplicações**, com foco em segurança de sistemas web e conformidade com a LGPD.

---

## 📌 Visão Geral do Projeto

A empresa FuturisTech está em expansão e precisa garantir que seus sistemas e APIs sejam acessados apenas por pessoas autorizadas, de forma segura e rastreável. Este projeto implementa controles técnicos e arquiteturais para proteger os dados da empresa e mitigar riscos de segurança cibernética.

---

## 🛠️ Componentes Modelados

- **Usuário Final (Human User)**: Interage com o sistema via navegador
- **Portal FuturisTech**: Aplicação Web protegida com autenticação federada (SSO)
- **API Gateway**: Roteador com validação de token JWT e controle de acesso
- **API Principal**: Responsável pela lógica de negócio e acesso aos dados
- **Servidor de Autenticação (Keycloak/Auth0)**: Autenticação SSO, MFA, login federado
- **Banco de Dados**: Armazena dados sensíveis com proteção por bcrypt/SHA-256
- **Logs de Auditoria**: Registros de atividade com proteção contra falsificação

---

## 🔒 Controles de Segurança Aplicados

- **Autenticação**: SSO, MFA, login com conta Google/Microsoft
- **Autorização**: RBAC (por função) e ABAC (por atributo)
- **Tokens JWT**: Validados no API Gateway com escopos e expiração
- **Criptografia**: bcrypt para senhas e SHA-256 para integridade
- **API Gateway**: Controle de tráfego, limitação de requisições e versionamento
- **Auditoria**: Logs com verificação de integridade e alerta de anomalias
- **Proteção LGPD**: Consentimento de cookies, privacidade e controle de dados

---

## 📁 Estrutura de Arquivos

```
/docs
  ├── projeto.pdf                 # Documento original do projeto
  ├── modelo.tm7                 # Arquivo do Microsoft Threat Modeling Tool
  ├── diagrama.png (opcional)   # Imagem do modelo visual
  ├── ameaças.csv (opcional)    # Lista de ameaças exportada
README.md
```

---

## 📋 Como visualizar o modelo

- Use o **Microsoft Threat Modeling Tool**
- Abra o arquivo `.tm7` e visualize os fluxos, componentes e ameaças
- Você também pode usar a versão em imagem para fins de apresentação

---

## 👩‍💻 Desenvolvido por

**Michele Pereira Martins**  
Módulo: Desenvolvimento Seguro de Aplicações

---

## 📌 Observações

Este projeto tem fins acadêmicos e demonstra boas práticas de segurança em arquitetura de aplicações modernas com foco em APIs e LGPD.
