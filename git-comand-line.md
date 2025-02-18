# Comandos Essenciais do Git

Este documento contém os principais comandos do **Git**, explicados de forma clara para facilitar o uso.

---

## ➡️ Configuração Inicial

### 1️. Configurar nome e e-mail (necessário para commits)
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```
Explicação: Define o nome e o e-mail que serão usados nos commits. A opção `--global` aplica as configurações para todos os repositórios do usuário.

---

## ➡️ Inicialização e Clonagem

### 2️. Criar um novo repositório Git
```bash
git init
```
Explicação: Inicializa um repositório Git no diretório atual. Um diretório oculto `.git/` é criado para armazenar o histórico.

### 3️. Clonar um repositório remoto
```bash
git clone <URL-do-repositorio>
```
Explicação: Cria uma cópia local de um repositório remoto, incluindo todo o histórico de commits.

---

## ➡️ Controle de Arquivos

### 4️. Verificar o status do repositório
```bash
git status
```
Explicação: Exibe os arquivos modificados, não rastreados e prontos para commit.

### 5️. Adicionar arquivos ao staging (área de preparação)
```bash
git add <arquivo>
# ou adicionar todos os arquivos modificados
git add .
```
Explicação: Move arquivos modificados para a área de staging, preparando-os para o commit.

---

## ➡️ Commits

### 6️. Criar um commit com uma mensagem descritiva
```bash
git commit -m "Mensagem do commit"
```
Explicação: Registra as mudanças no histórico do repositório.

### 7️. Alterar a mensagem do último commit (caso ainda não tenha sido enviado)
```bash
git commit --amend -m "Nova mensagem do commit"
```
Explicação: Modifica o último commit, permitindo corrigir mensagens ou adicionar novos arquivos.

---

## ➡️ Branches

### 8️. Criar uma nova branch
```bash
git branch <nome-da-branch>
```
Explicação: Cria uma nova branch sem mudar para ela.

### 9️. Mudar para uma branch existente
```bash
git checkout <nome-da-branch>
# ou no Git mais recente:
git switch <nome-da-branch>
```
Explicação: Alterna entre branches.

### 🔟 Criar e mudar para uma nova branch ao mesmo tempo
```bash
git checkout -b <nome-da-branch>
# ou no Git mais recente:
git switch -c <nome-da-branch>
```
Explicação: Cria uma nova branch e já muda para ela.

---

## ➡️ Merge e Rebase

### 1️.1️. Mesclar uma branch na atual
```bash
git merge <nome-da-branch>
```
Explicação: Combina as alterações de uma branch na branch atual.

### 1️.2️. Rebase (reescrevendo histórico)
```bash
git rebase <nome-da-branch>
```
Explicação: Move commits da branch atual para o topo da branch especificada, criando um histórico linear.

---

## ➡️ Repositórios Remotos

### 1️.3️. Adicionar um repositório remoto
```bash
git remote add origin <URL-do-repositorio>
```
Explicação: Conecta o repositório local a um remoto.

### 1️.4️. Enviar commits para o repositório remoto
```bash
git push origin <nome-da-branch>
```
Explicação: Envia as alterações da branch atual para o repositório remoto.

### 1️.5️. Baixar alterações do repositório remoto
```bash
git pull origin <nome-da-branch>
```
Explicação: Atualiza a branch local com as mudanças do repositório remoto.

---

## 🕒 Histórico e Reversão

### 1️.6️. Exibir o histórico de commits
```bash
git log
```
Explicação: Mostra uma lista dos commits com autor, data e mensagens.

### 1️.7️. Ver diferenças entre arquivos antes do commit
```bash
git diff
```
Explicação: Exibe as alterações feitas nos arquivos antes de serem commitadas.

### 1️.8️. Reverter um commit sem apagar o histórico
```bash
git revert <hash-do-commit>
```
Explicação: Cria um novo commit que desfaz as mudanças do commit especificado.

### 1️.9️. Resetar para um commit específico (com perda de alterações locais)
```bash
git reset --hard <hash-do-commit>
```
Explicação: Retorna o repositório para um estado anterior, descartando mudanças.

---

## 🚀 Conclusão
Estes são os comandos essenciais para trabalhar com o Git. Com eles, é possível criar, versionar, reverter e compartilhar código de maneira eficiente! 🔥
