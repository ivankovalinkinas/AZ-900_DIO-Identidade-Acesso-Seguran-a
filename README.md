# Identidade, Acesso e Segurança no Azure (AZ-900)

Este resumo aborda os conceitos sobre **identidade, controle de acesso e segurança** dentro do Microsoft Azure.

---

## 🔑 Identidade

### O que é

* Identidade é a base para **autenticação** e **autorização** no Azure, o serviço principal para a gestão de identidade é o **Microsoft Entra ID**.

### Características

* Gerenciamento centralizado de usuários, grupos e dispositivos.
* Suporte a autenticação **SSO**, permitindo o acesso em diversos aplicativos após um único login.
* Integração com ambientes locais AD DS, através do aplicativo Microsoft Entra Connect.
* Possibilidade de autenticação multifator (**MFA**) para maior segurança.

### Benefícios

* **Centralização:** um único diretório para gerenciamento de identidades, seja ela local (AD DS) ou na nuvem.
* **Segurança:** políticas de acesso condicional e MFA.

---

## 🛡️ Acesso

### O que é

* Controle sobre **quem pode acessar** determinados recursos no Azure e **quais ações** podem ser executadas, nível de permissonamento que será concedido.

### Ferramentas principais

* **RBAC (Role-Based Access Control):** define permissões baseadas em funções (ex.: leitor, colaborador, administrador).
* **Acesso Condicional:** aplica regras de acesso baseadas em sinais (local, dispositivo, risco, geografia, etc).
* **Privileged Identity Management (PIM):** fornece acesso administrativo sob demanda, reduzindo riscos (administrador pode não precisar ser administrador por 24h). 

### Benefícios

* **Granularidade:** permissões específicas por recurso, grupo ou usuário.
* **Segurança:** evita privilégios excessivos.

---

## 🔒 Segurança

### O que é

* Conjunto de serviços e práticas que protegem dados, identidades e recursos no Azure.

### Principais serviços

* **Microsoft Defender for Cloud:** monitoramento de segurança, recomendações e proteção contra ameaças.
* **Key Vault:** armazenamento seguro de chaves, segredos e certificados.
* **Azure Firewall:** firewall gerenciado para proteger redes virtuais.
* **DDoS Protection:** proteção contra ataques de negação de serviço.

### Benefícios

* **Visibilidade:** alertas sobre vulnerabilidades ou possíveis melhorias no ambiente.
* **Proteção:** defesa contra ataques e falhas de configuração.

### *Modelo Defesa em Profundidade*
```
 ---------------------------------
 |  Segurança Física             |
 | ----------------------------  |
 | | Identidade e Acesso       | |
 | | ------------------------  | |
 | | | Perímetro             | | |
 | | | --------------------- | | |
 | | | | Rede              | | | |
 | | | | ----------------- | | | |
 | | | | | Computação    | | | | |
 | | | | | ------------- | | | | |
 | | | | | |Aplicativo | | | | | |
 | | | | | | --------  | | | | | |
 | | | | | | |Dados |  | | | | | |
 | | | | | | --------  | | | | | |
 | | | | | ------------- | | | | |
 | | | | ----------------- | | | |
 | | | --------------------- | | |
 | | ------------------------  | |
 | ----------------------------  |
 ---------------------------------
```

## 📌 Conclusão

* **Identidade:** base para autenticação/autorização via Entra ID (Azure AD).
* **Acesso:** gerenciado via RBAC, Acesso Condicional e PIM.
* **Segurança:** garantida por um conjunto de serviços (Defender, Firewall, Key Vault, DDoS Protection, etc).

---
