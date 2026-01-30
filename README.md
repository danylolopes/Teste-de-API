# Testes Automatizados de API 

Este repositório contém a implementação de testes automatizados de API desenvolvidos
como parte de um desafio técnico, utilizando **Postman** e integrados a uma pipeline
de **CI com GitHub Actions**.

---

## 📌 Objetivo
Validar os principais endpoints da API, garantindo:
- Funcionamento correto do CRUD de usuários
- Autenticação via token (JWT)
- Testes positivos e negativos
- Execução automatizada em pipeline de CI
- Geração de relatórios como artefato

---

## 🛠️ Tecnologias Utilizadas
- Postman
- Postman CLI
- GitHub Actions
- Git

---

## 📂 Estrutura do Projeto

```
├── tests/
│ ├── collection.json # Collection Postman com os testes
│ └── environment.json # Environment com variáveis
│
├── .github/
│ └── workflows/
│ └── api-tests.yml # Pipeline de CI
│
└── README.md
```


---

## ▶️ Execução Local (Postman)

1. Importar os arquivos `collection.json` e `environment.json` no Postman
2. Selecionar o environment **API-Test-Env**
3. Executar os testes utilizando o **Collection Runner**
4. Validar os resultados diretamente no Postman

---

## 🤖 Execução em CI (GitHub Actions)

A pipeline é executada automaticamente a cada:
- Push
- Pull Request

Fluxo da pipeline:
1. Checkout do repositório
2. Execução da collection via **Postman CLI**
3. Geração de relatórios em formato **JUnit** e **HTML**
4. Publicação dos relatórios como **artefatos da pipeline**

Os relatórios podem ser acessados na aba **Actions** do GitHub.

---

## 📊 Relatórios
- `JUnit XML`: utilizado para análise automatizada na pipeline
- `HTML`: utilizado para visualização manual dos resultados

---

## 📎 Observações
- O projeto não utiliza Newman, conforme solicitado no desafio
- As variáveis sensíveis são gerenciadas via Environment do Postman
- O delay entre requisições respeita limites de rate limit da API

---

## 👨‍💻 Autor
 **Danylo Amorim Lopes**


