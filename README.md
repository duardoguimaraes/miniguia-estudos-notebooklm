# 📚 Miniguia de Estudos: Git e GitHub para Iniciantes
> **Caderno Temático criado com Inteligência Artificial (NotebookLM)** para o Desafio de Projeto da [Digital Innovation One (DIO)](https://www.dio.me/).

---

## 🎯 Contexto e Objetivos

### Contexto
O controle de versão com **Git** e o uso do **GitHub** são competências essenciais para qualquer pessoa que deseja ingressar no mercado de desenvolvimento de software e tecnologia. No entanto, iniciantes frequentemente enfrentam dificuldades com a terminologia (*commit*, *pull request*, *merge*, *branch*), com a linha de comando e com a compreensão do fluxo de trabalho colaborativo.

Este projeto utiliza o **NotebookLM** como ferramenta de aprendizagem ativa para analisar fontes confiáveis, sintetizar conceitos cruciais e gerar um material prático de consulta rápida.

### Objetivos de Estudo
* **Compreender a arquitetura básica do Git**: entender a diferença entre repositório local, *staging area* e repositório remoto.
* **Dominar o fluxo essencial de comandos**: aprender os comandos do dia a dia (`init`, `add`, `commit`, `push`, `pull`, `status`).
* **Desmistificar o GitHub**: entender conceitos de colaboração, como *forks*, *pull requests*, *issues* e gerenciamento de conflitos de *merge*.
* **Desenvolver habilidades de Engenharia de Prompts**: aprender a formular perguntas estratégicas para IAs com base em documentos técnicos.

---

## 📑 Curadoria de Fontes

Para alimentar o NotebookLM e garantir respostas precisas e fundamentadas (sem alucinações), foram selecionadas as seguintes fontes abertas e documentações oficiais:

1. **[Git Documentation - Getting Started (Oficial)](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)**
   * *Descrição:* Documentação oficial do Git cobrindo os fundamentos do controle de versão e os três estados do Git.
2. **[GitHub Docs - GitHub Glossary](https://docs.github.com/pt/get-started/learning-about-github/github-glossary)**
   * *Descrição:* Glossário oficial do GitHub detalhando a terminologia de colaboração remota.
3. **[Atlassian Git Tutorial - Basic Git Commands](https://www.atlassian.com/git/tutorials/setting-up-a-repository)**
   * *Descrição:* Artigo explicativo sobre a criação de repositórios, preparação de arquivos (*staging*) e histórico de commits.

---

## 🛠️ Engenharia de Prompts, Testes e "Cicatrizes" (Troubleshooting)

Nesta seção estão registrados os testes de prompts aplicados no NotebookLM, os ajustes necessários para obter melhores respostas e os aprendizados do processo.

### 📜 Teste 1: Explicação do Fluxo Básico do Git

* **Prompt Inicial:** *"Me explica como funciona o Git."*
  * **Resultado:** Resposta genérica, muito teórica e abrangente. Não focou no fluxo prático do iniciante.
* **Prompt Refinado:** *"Com base nos documentos fornecidos, explique o fluxo de trabalho básico do Git para um iniciante em 4 passos simples. Inclua a relação entre Working Directory, Staging Area e Local Repository."*
  * **Resultado Obtido:** A IA estruturou com precisão o fluxo (*Edit* -> *Stage* -> *Commit* -> *Push*), citando diretamente as seções das fontes.

---

### 📜 Teste 2: Diferença entre Git e GitHub

* **Prompt Inicial:** *"Qual a diferença de Git e GitHub?"*
  * **Resultado:** Resposta clara, mas faltaram analogias para fixar o conceito.
* **Prompt Refinado:** *"Explique a diferença entre Git e GitHub usando uma analogia simples do mundo real. Mantenha a explicação focada na função de cada um no desenvolvimento de software."*
  * **Resultado Obtido:** A IA utilizou a analogia de um **Editor de Texto/Caderno de Anotações (Git)** versus uma **Biblioteca/Nuvem de Compartilhamento (GitHub)**, facilitando imensamente a compreensão.

---

### ⚠️ Cicatrizes & Troubleshooting (Dificuldades Encontradas)

* **Problema:** Ao perguntar como resolver um *merge conflict*, a IA gerou comandos avançados (`git rebase`, `git cherry-pick`) que fogem do escopo para iniciantes.
* **Causa:** O prompt não delimitou o nível de senioridade e o contexto prático desejado.
* **Solução:** O prompt foi reescrito adicionando a restrição de público: *"Explique como resolver um conflito de merge simples usando apenas comandos básicos (`git status`, edição manual do arquivo e `git commit`), direcionado a quem está no primeiro dia de uso do Git."*

---

## 📖 Miniguia de Estudo: Git e GitHub para Iniciantes

### 🔍 1. Resumo Estruturado do Assunto

#### O que é Git?
O **Git** é um sistema de controle de versão distribuído (*DVCS*). Ele registra as alterações feitas em um conjunto de arquivos ao longo do tempo, permitindo que você volte a versões específicas, recupere arquivos perdidos e trabalhe em equipe sem sobrescrever o trabalho de outros.

#### Os Três Estados do Git
1. **Working Directory (Diretório de Trabalho):** Onde você cria e edita seus arquivos no dia a dia.
2. **Staging Area (Área de Preparação / Index):** Onde você seleciona quais alterações específicas farão parte do próximo "retrato" (snapshot) do projeto.
3. **Local Repository (Repositório Local):** Onde o Git salva permanentemente os snapshots (*commits*) no histórico da sua máquina.

#### Fluxo de Comandos Essenciais

```bash
# 1. Inicializar o repositório na pasta atual
git init

# 2. Verificar o estado dos arquivos
git status

# 3. Adicionar arquivos à Staging Area
git add nome-do-arquivo.txt    # Arquivo específico
git add .                      # Todos os arquivos alterados

# 4. Salvar as alterações no repositório local
git commit -m "feat: adiciona estrutura inicial do projeto"

# 5. Conectar ao repositório remoto (GitHub)
git remote add origin [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)

# 6. Enviar suas alterações para o GitHub
git push -u origin main

### 📘 2. Glossário de Conceitos-Chave

* **Repository (Repositório):** A "pasta" do seu projeto onde o Git armazena todo o histórico de alterações e arquivos de configuração.
* **Commit:** Um *snapshot* (ponto de restauração) do seu código em um determinado momento. Cada commit possui uma mensagem explicativa e um identificador único (*hash*).
* **Branch (Ramificação):** Uma linha independente de desenvolvimento. Permite criar novas funcionalidades sem afetar o código principal (`main`).
* **Merge:** O ato de mesclar o histórico e as alterações de uma *branch* secundária para a *branch* principal.
* **Fork:** Uma cópia independente de um repositório de outro usuário salva na sua conta do GitHub.
* **Pull Request (PR):** Uma solicitação enviada ao dono do repositório para que ele analise e aceite incorporar as suas alterações ao código principal.
* **Clone:** O ato de baixar uma cópia exata de um repositório remoto (GitHub) para a sua máquina local.

---

### 🔄 3. Prompts Reutilizáveis para Revisão Futura

Guarde estes prompts para utilizar no NotebookLM ou em outras IAs sempre que precisar revisar conceitos de Git e GitHub:

> 🤖 **Prompt para Explicar Comandos:**
> *"Atue como um instrutor de programação didático. Explique a função do comando `git [INSERIR_COMANDO]` para um iniciante, mostrando um exemplo prático de uso e o que acontece nos bastidores do repositório."*

> 🤖 **Prompt para Resolução de Erros:**
> *"Estou recebendo o seguinte erro no terminal ao tentar usar o Git: `[COLE_O_ERRO_AQUI]`. Explique o que esse erro significa em linguagem simples e forneça um passo a passo seguro para corrigi-lo."*

> 🤖 **Prompt de Simulação de Quiz:**
> *"Crie um quiz com 5 perguntas de múltipla escolha sobre a diferença entre comandos do Git local e ações no GitHub remoto. Forneça o gabarito comentado ao final."*

---

## 🤝 Considerações Finalização e Entregáveis

Este material foi construído unindo curadoria humana e capacidade analítica da IA (**NotebookLM**), demonstrando como a Inteligência Artificial pode potencializar a documentação e o aprendizado contínuo na área de tecnologia.

---
*Projeto desenvolvido como parte do Desafio de Projeto da **DIO**.*



