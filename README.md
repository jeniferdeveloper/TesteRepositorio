##### GIT #####
O Git (Sistema de Controle de Versão Local) é um sistema de controle de versão distribuído (DVCS), criado por Linus Torvalds (o mesmo criador do Linux). 
Ele permite que você gerencie diferentes versões do seu código de forma eficiente.

## Principais Funções do Git
Função	                               Descrição
Controle de versão	                   Salva o histórico de todas as alterações no código.
Branching (Ramificações)	             Permite criar "linhas alternativas" do projeto (branches) para desenvolver features separadamente.
Merging (Mesclagem)	                   Combina diferentes branches em uma versão final.
Staging Area	                         Área intermediária onde você seleciona quais mudanças serão salvas no próximo commit.
Trabalho offline	                     Como o Git é local, você pode versionar sem internet.

## 🛠 Recursos Principais do Git
1. Repositório Local
Diretório oculto .git que armazena todo o histórico e configurações.
Inicializado com:
git init

2. Sistema de Branches
Branch principal: Tradicionalmente chamada master, agora muitas usam main.
Comandos úteis:
git branch                      # Lista branches
git branch nova-feature         # Cria nova branch
git checkout nova-feature       # Muda para a branch
git merge nova-feature          # Mescla a branch atual

3. Sistema de Commits
Cada commit é um snapshot do projeto naquele momento.
Boas práticas:
Commits atômicos (uma mudança por commit)
Mensagens claras (ex: "Corrige bug no login")
git commit -m "mensagem descritiva"

5. Trabalho com Remotos
Conexão com repositórios remotos (GitHub, GitLab etc.):
git remote add origin URL       # Adiciona um remote
git push -u origin main        # Envia commits
git pull origin main          # Atualiza local

5. Resolução de Conflitos
Quando o Git não consegue mesclar alterações automaticamente:
Edita os arquivos com conflitos (marcados com <<<<<<<)
Adiciona as alterações resolvidas:
git add arquivo-conflitante
git commit

## COMANDOS
⌨️ Comandos Básicos do Git (Para Trabalhar com GitHub)
Comando	                             O que Faz?
git init	                           Inicializa um repositório Git local.
git clone                            URL	Baixa um repositório do GitHub.
git add .	                           Adiciona arquivos ao Staging Area.
git commit -m "mensagem"	           Salva as alterações no histórico.
git push origin main	               Envia alterações para o GitHub.
git pull origin main	               Puxa atualizações do GitHub.
git branch	                         Lista todas as branches.
git checkout -b nova-branch	         Cria e muda para uma nova branch.
git merge branch	                   Mescla uma branch com a atual.
git status	                         Mostra o estado atual do repositório.

⌨️ Comandos Essenciais do Git
Configuração Inicial
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
git config --global init.defaultBranch main  # Define branch padrão

*Fluxo Básico de Trabalho
git init                         # Inicia repositório
git add .                        # Adiciona arquivos ao stage
git commit -m "Primeiro commit"  # Cria commit
git status                       # Verifica estado atual

*Trabalhando com Branches
git branch                       # Lista branches
git checkout -b nova-branch      # Cria e muda para nova branch
git merge outra-branch           # Mescla branches

*Sincronizando com Remotos
git clone URL                    # Clona repositório remoto
git push origin main             # Envia alterações
git pull origin main            # Atualiza local

*Desfazendo Ações
git reset --soft HEAD~1         # Remove commit mas mantém alterações
git reset --hard HEAD~1         # Descarta commit e alterações
git checkout -- arquivo         # Descarta mudanças não commitadas

*Visualizando Histórico
git log                          # Mostra histórico completo
git log --oneline                # Histórico resumido
git diff                         # Mostra alterações não commitadas

## 💡 Dicas Avançadas
.gitignore: Arquivo para excluir arquivos desnecessários (ex: node_modules/, .env)
echo "node_modules/" > .gitignore

Stashing: Guarda alterações temporárias sem commit
git stash                     # Guarda alterações
git stash pop                 # Recupera alterações

Rebase vs Merge:
merge: preserva histórico completo (mais seguro)
rebase: cria histórico linear (mais limpo)
Tags: Marca versões importantes (ex: v1.0.0)
git tag -a v1.0.0 -m "Versão 1.0"
git push origin v1.0.0

## 🎯 Quando Usar o Git?
✅ Qualquer projeto de software (mesmo individual)
✅ Quando precisa de histórico de alterações
✅ Trabalho em equipe (combinado com GitHub/GitLab)
✅ Gerenciamento de versões (tags, releases)
O Git é essencial para qualquer desenvolvedor moderno! 🚀 Quer um guia mais detalhado sobre algum aspecto específico?

#### GITHUB ####
O GitHub(Plataforma de Hospedagem de Código) é uma plataforma de hospedagem de código baseada em Git. Ele adiciona funcionalidades extras, como colaboração em equipe, 
pull requests, issues e integração com ferramentas de CI/CD.

## Principais Funções do GitHub
Função	                               Descrição
Hospedagem de repositórios	           Armazena projetos Git na nuvem.
Colaboração	                           Permite que várias pessoas trabalhem no mesmo projeto.
Pull Requests	                         Sistema de revisão de código antes de mesclar alterações.
GitHub Pages	                         Hospeda sites estáticos gratuitamente (HTML, CSS, JS).
GitHub Actions	                       Automação de testes e deploy (CI/CD).

## 🛠 Recursos Principais do GitHub
1. Repositórios (Repos)
Armazenam código-fonte, documentação e arquivos.
Públicos (qualquer um pode ver) ou privados (somente pessoas autorizadas).
README.md: Arquivo de apresentação do projeto (suporta Markdown).

2. Branches (Ramificações)
Permitem trabalhar em features separadas sem afetar o código principal (main/master).
Comandos Git:
git branch nome-da-branch      # Cria uma nova branch
git checkout nome-da-branch    # Muda para a branch
git merge nome-da-branch       # Mescla a branch com a main

3. Pull Requests (PRs)
Solicitação de mesclagem de uma branch para a main.
Permite revisão de código antes do merge.
Fluxo típico:
Cria uma branch → faz alterações → abre um PR.
Outros revisam → aprovam → fazem merge.

4. GitHub Issues
Usado para:
Reportar bugs.
Sugerir melhorias.
Discutir ideias.
Pode ser vinculado a PRs e milestones.

5. GitHub Actions (CI/CD)
Automatiza testes, builds e deploys.
Exemplo de fluxo:
Toda vez que um PR é aberto, roda testes automaticamente.
Se passar, faz deploy em produção.
Configurado via arquivo .github/workflows/main.yml.

6. GitHub Pages
Hospeda sites estáticos gratuitamente.
Como publicar:
Crie uma branch gh-pages ou use main.
Vá em Settings > Pages e selecione a branch.
Seu site estará em:
https://seu-usuario.github.io/nome-do-repo/

7. GitHub Projects
Quadro Kanban para organizar tarefas.
Pode ser vinculado a Issues e PRs.

## 🔹 Comparação: GitHub vs. Git
Recurso	                     Git (Local)	       GitHub (Nuvem)
Armazenamento	                No seu PC	         Na nuvem
Histórico	                       Sim	           Sim (sincronizado)
Colaboração	                  Limitada	         Avançada (PRs, Issues)
Hospedagem de Sites	           ❌ Não	         ✅ Sim (GitHub Pages)
Automação (CI/CD)	             ❌ Não	           ✅ Sim (GitHub Actions)

## 🎯 Quando Usar o GitHub?
✅ Trabalho em equipe (open source ou empresa).
✅ Quer hospedar um site estático (GitHub Pages).
✅ Precisa de automação (GitHub Actions).
✅ Quer backup do código na nuvem.
Se for um projeto pessoal pequeno, você pode usar apenas Git local. Mas para colaboração e recursos avançados, o GitHub é essencial! 🚀

#### 🔹 Git vs. GitHub: Entenda a Diferença
Característica	               Git	                               GitHub
O que é	                       Sistema de controle de versão	     Plataforma de hospedagem de código
Onde roda	                     Local na sua máquina	               Serviço online
Funciona offline?              Sim	                               Não (exceto para ações locais)
Recursos de colaboração	       Básico	                             Avançado (PRs, Issues, Projects)
Hospedagem	                   Não	                               Sim
CI/CD	                         Não	                               Sim (GitHub Actions)

## Comparação: Git vs. Upload Manual
Método	Requer Git?	   Vantagens	      Desvantagens
Upload pelo site	     ❌ Não	          Rápido, não precisa instalar nada	Não versiona histórico local
GitHub Desktop	       ❌ Não (GUI)	    Interface amigável, versionamento	Precisa instalar o app
Git (terminal)	       ✅ Sim	          Mais controle, histórico completo	Requer conhecimento de comandos

## Quando Usar Cada Método?
Upload manual: Ideal para arquivos únicos ou projetos pequenos.
GitHub Desktop: Bom para quem não quer usar terminal, mas ainda quer versionamento.
Git (CLI): Melhor para projetos grandes e colaboração avançada.
Se você só quer subir arquivos rapidamente, o upload manual pelo site é a melhor opção! 🚀


#### SUBIR ARQUIVOS SEM INSTALAR O GIT 

É possível subir arquivos para o GitHub sem instalar o Git diretamente no seu computador. Você pode fazer isso de duas formas:

1. Pelo Próprio Site do GitHub (Upload Manual)
Passo a Passo:
Acesse o GitHub (github.com) e faça login.
Crie um novo repositório (ou abra um existente).
Clique no botão "Add file" (canto superior direito) > "Upload files".
Arraste e solte os arquivos ou clique em "choose your files" para selecioná-los.
Adicione uma mensagem de commit (opcional, mas recomendado).
Clique em "Commit changes" para finalizar.

2. Usando o GitHub Desktop (Sem Comandos no Terminal)
Se você não quer usar o terminal, mas ainda deseja uma ferramenta gráfica para gerenciar repositórios, pode usar o GitHub Desktop:
Baixe e instale GitHub Desktop.
Faça login com sua conta do GitHub.
Crie/Clone um repositório.
Arraste os arquivos para a pasta do repositório.
Descreva as alterações e clique em "Commit to main".
Clique em "Push origin" para enviar ao GitHub.

✅ Pronto! Seus arquivos já estarão no GitHub.
