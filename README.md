

# Git Learning – Minhas anotações pessoais de Git 🚀

[![Estudando Git](https://img.shields.io/badge/Estudando-Git-blue?logo=git&logoColor=white)](https://github.com/Bussola2015/Git-Learning)
[![Última atualização](https://img.shields.io/github/last-commit/Bussola2015/Git-Learning?color=green)](https://github.com/Bussola2015/Git-Learning)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Olá! 👋  
Esse repositório é o meu **caderno de estudos vivo** sobre Git e GitHub.  
Comecei do zero em setembro de 2025 e vou atualizando conforme aprendo coisas novas nos projetos reais.

Aqui não tem enrolação nem teoria chata: só comandos que eu realmente uso, exemplos práticos e dicas que me salvaram várias vezes.

Perfeito pra quem tá começando ou quer um cheat sheet rápido.

---

## Índice rápido
- [Comandos básicos](#comandos-básicos)
- [Fluxo de trabalho que eu uso todo dia](#meu-fluxo-de-trabalho-diário)
- [Branchs, merge e rebase](#branchs-merge-e-rebase)
- [Dicas que ninguém conta](#dicas-que-ninguém-conta)
- [Como usar essas notas](#como-usar-essas-notas)

---

## Comandos básicos

| Comando                  | O que faz                                      | Exemplo comum                          |
|--------------------------|------------------------------------------------|----------------------------------------|
| `git init`               | Cria um repositório novo                      | `git init meu-projeto`                 |
| `git clone <url>`        | Baixa um repo existente                        | `git clone https://github.com/...`     |
| `git add .`              | Adiciona tudo pro stage                        | `git add .`                            |
| `git commit -m "msg"`    | Salva as mudanças com mensagem                 | `git commit -m "feat: adiciona login"` |
| `git push origin main`   | Envia pro GitHub                               | `git push origin main`                 |
| `git pull`               | Atualiza seu repo local com o remoto           | `git pull`                             |
| `git status`             | Mostra o que tá acontecendo (meu melhor amigo) | `git status`                           |
| `git log --oneline`      | Histórico resumido                             | `git log --oneline`                    |

---

## Meu fluxo de trabalho diário (o que eu realmente faço)

```bash
# 1. Atualizo tudo
git pull

# 2. Crio branch com nome descritivo
git checkout -b feature/nova-tela-login

# 3. Faço as alterações → salvo → commit pequeno
git add .
git commit -m "feat: cria formulário de login"

# 4. Subo a branch
git push origin feature/nova-tela-login

# 5. Abro o Pull Request no GitHub → reviso → mergeio

## Branchs, merge e rebase

| Comando                              | Quando uso                                              |
|--------------------------------------|---------------------------------------------------------|
| `git checkout -b nome-branch`        | Criar e já entrar na branch                             |
| `git switch main` / `git checkout main` | Voltar pra main                                      |
| `git merge nome-branch`              | Juntar branch na atual (geralmente faço pelo GitHub)   |
| `git rebase main`                    | Quando quero deixar o histórico linear (amo!)           |
| `git branch -d nome-branch`          | Apagar branch local depois do merge                     |

## Dicas que ninguém conta

- **Nunca** commite direto na `main` → sempre crie uma branch!
- Use `git stash` quando precisa trocar de branch rápido e tem mudanças não commitadas.
- `.gitignore` é seu amigo número 1 (tem um exemplo na raiz desse repo).
- Mensagens de commit: em projetos pessoais eu misturo, mas em projetos públicos/fora do Brasil eu uso inglês.
- `git log --graph --all --oneline` → gera uma arte ASCII linda do histórico do projeto.

## Como usar essas notas

1. Clone o repo  
   ```bash
   git clone https://github.com/Bussola2015/Git-Learning.git
