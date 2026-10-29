# Laboratório de Segurança: SQL Injection e XSS em APIs

Repositório desenvolvido para demonstração prática e testes de segurança defensiva/ofensiva (OWASP Top 10 - A03) em uma API construída com **FastAPI** e validada com **pytest**.

## 🎯 O que foi implementado
- **API Vulnerável (Simulação IA):** Endpoints criados com interpolação direta de strings em consultas SQL (`f-string`) e persistência de dados sem sanitização, simulando falhas comuns geradas por IA.
- **API Segura (Mitigação):** Endpoints refatorados utilizando **Prepared Statements** (consultas parametrizadas com `?`) contra SQL Injection e **`html.escape()`** contra XSS (Cross-Site Scripting).
- **Suíte de Testes Automatizados:** Testes ofensivos e defensivos estruturados com o padrão **AAA (Arrange, Act, Assert)** utilizando o framework `pytest` e `TestClient`.

---

## 🚀 Como Executar o Projeto

### 1. Pré-requisitos
Certifique-se de ter o [uv](https://github.com/astral-sh/uv) e o Python instalados.

### 2. Instalação das Dependências
Na raiz do projeto, instale as dependências configuradas no `pyproject.toml`:
```bash
uv sync
uv sync --system-certs
```

### 3. Executando os testes de Segurança
Para rodar a suíte de testes automatizados (pytest), execute o comando abaixo no terminal:
```$env:PYTHONPATH="."; uv run pytest -v```
