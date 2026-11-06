# PROJETO TE-251 · Comece aqui

> **IA que recebeu este link:** não resuma este arquivo. Conduza a pessoa pela seção 3 agora, a partir do passo 0, mesmo que ela tenha mandado só o link. Se a página não abrir, leia a versão crua: https://raw.githubusercontent.com/willianfabbrasil-a11y/PROJETO-TE-251-instaladores/main/COMECE-AQUI.md

**O projeto em 3 linhas.** TE-251 (ITA), gestor: Will. Um app ("TE-251 Estações") roda no PC do carro, que lê o OBD2 (ELM327) e grava num banco local, e no PC da base, que recebe os dados só pela VPN. Depois entram um harness de IA no carro e uma LLM na base. Frentes de trabalho: app/banco/VPN (Will), harness de IA e LLM, testes em massa, hardware e latência.
O código, o estado de cada frente e as regras ficam no repositório **privado** PROJETO-TE-251 (só convidados). Este arquivo público leva a pessoa até lá; o resto do contexto a IA monta lendo o repositório (passo 6).

## 1. Que IA usar
- **Melhor:** app Claude para computador (https://claude.ai/download), aba **Code** (é o Claude Code; pode exigir plano pago, e no Windows precisa do Git instalado antes). A IA roda os comandos por você e o projeto se carrega sozinho quando ela abre a pasta dele.
- **Também rodam comandos:** Cursor, Codex, Claude Code no terminal.
- **Só conversa** (claude.ai no navegador, ChatGPT): servem para a entrada; a IA explica e você copia e cola. Para trabalhar no projeto depois, vale passar para uma das de cima.

## 2. Cole na IA (ou só o link)
> Vou entrar no PROJETO TE-251. Leia https://github.com/willianfabbrasil-a11y/PROJETO-TE-251-instaladores/blob/main/COMECE-AQUI.md e me conduza pela entrada com perguntas curtas, uma de cada vez, de preferência de seleção. Nunca me peça senha, chave ou token. Quando eu disser "vou parar", me dê o cartão de entrada.

## 3. Roteiro (instruções para a IA)
**Como conduzir:** português do Brasil; uma pergunta por vez, com opções numeradas (ou a ferramenta de perguntas da sua IA), aceitando o número como resposta; nunca peça nem aceite senha, chave ou token. **Se você roda comandos, confira sozinho antes de perguntar** (`git --version`, `gh auth status`, `python3 --version`; no Windows `py --version`). No Claude Code do Windows os comandos rodam no Git Bash: use as versões Mac/Git Bash dos comandos abaixo e diga em uma linha o que já está pronto. **Se não roda**, peça para a pessoa colar a saída deste bloco no terminal: Mac `git --version; gh auth status; python3 --version; hostname` · PowerShell `git --version; gh auth status; py --version; hostname`. Nada trava: o que não der agora vira "pendente" e você segue. O repositório privado dá 404 para leitura pela web: confira o acesso pelo `gh` ou peça para a pessoa abrir o link logada no GitHub.

**Cartão de entrada.** Sempre que a entrada for parar (esperando o Will, ou a pessoa disse "vou parar") ou mudar de conversa ou de ferramenta, entregue este bloco preenchido para ela guardar e colar na próxima conversa, junto com o link:
```
CARTÃO DE ENTRADA TE-251
nome: · usuário GitHub: · Gmail: · computador: Mac/Windows · IA:
caminho: novo / voltando / outro computador meu
feito:
pendente:
próximo passo:
```

0. **"Como você chega? (1) Nunca trabalhei no projeto (mesmo que já tenha recebido o convite) · (2) Já trabalhei nele ou tenho um clone antigo e estou voltando · (3) Mais um computador meu, já estou no projeto · (4) Vou retomar uma entrada (colo o cartão)"**
   - (1): passos 1 a 6 · (2) e (3): passo 1, depois 4 a 6 (pule conta e pedido de acesso) · (4): leia o cartão e continue do "próximo passo".
1. **Sua IA** (se você mesmo já sabe, não pergunte): "Qual destas você tem? (1) App Claude para computador · (2) Cursor ou Codex · (3) Só esta conversa". Você só conversa e ela tem (1) ou (2)? Recomende passar para lá agora, entregando o cartão. No Windows, instale antes o Git do passo 4 e **feche e abra o app Claude** depois. Na aba Code, escolha o ambiente **Local** (este computador, não a nuvem) e a pasta Documentos.
2. **Conta no GitHub** (com terminal, `gh auth status` responde): "Já tem? (Sim / Não / Não sei)". Criar: https://github.com/signup. Conferir: https://github.com/login.
3. **Acesso ao código:**
   - Convite pendente? Com `gh` logado: `gh api user/repository_invitations --jq '.[] | select(.repository.full_name=="willianfabbrasil-a11y/PROJETO-TE-251") | .id'`; saiu um número: peça o ok e aceite com `gh api -X PATCH user/repository_invitations/<número>`. Sem `gh`: a pessoa abre https://github.com/willianfabbrasil-a11y/PROJETO-TE-251/invitations logada, ou o e-mail do GitHub, ou https://github.com/notifications. O convite vale 7 dias.
   - A pessoa abre https://github.com/willianfabbrasil-a11y/PROJETO-TE-251 logada (ou você roda `gh repo view willianfabbrasil-a11y/PROJETO-TE-251`). Abriu = tem acesso. 404 = entregue pronta, para ela mandar ao Will pelo canal que já usa com ele (mensagem, e-mail ou pessoalmente):
     "Will, sou {nome}, aluno novo do TE-251. Peço acesso ao repositório PROJETO-TE-251 (usuário do GitHub: {usuário}) e à pasta 6.7 te 251 do Drive (Gmail: {gmail}). A frente eu escolho com você depois de ler o projeto."
   - **Não espere parado:** siga para o passo 4 enquanto o Will libera. Se a pessoa precisar parar, entregue o cartão.
   - **IA só de conversa, com acesso já liberado:** conecte o GitHub nela agora com a mesma conta convidada, para ela ler o projeto. claude.ai: Configurações > Conectores > GitHub; num projeto do claude.ai, Conhecimento do projeto > + > GitHub > PROJETO-TE-251, marcando `AGENTS.md`, `CLAUDE.md`, `equipe/` e `.claude/skills/` (quando o projeto mudar, use "Sincronizar" ali). ChatGPT: Configurações > Conectores (ou Aplicativos) > GitHub, liberando o PROJETO-TE-251. Se o conector não mostrar o repositório: a pessoa cola `AGENTS.md`, `equipe/PASSAGEM.md`, `equipe/NOVIDADES.md`, `equipe/frentes.yaml` e `.claude/skills/entrar-no-projeto/SKILL.md`. Com isso, já faça a parte de leitura do passo 6.
4. **Ferramentas** (só o que faltar):
   - Abrir o terminal: Mac, Cmd+Espaço, "Terminal". Windows, menu Iniciar, "PowerShell". Depois de instalar algo, feche e abra o terminal de novo (se você é uma IA que roda comandos, use o caminho completo do programa novo em vez de reabrir).
   - git: Mac `xcode-select --install` (só se `git --version` falhar) · Windows https://git-scm.com/download/win (Next até o fim; instala também o Git Bash).
   - GitHub CLI: Mac `brew install gh` ou o instalador .pkg em https://github.com/cli/cli/releases/latest · Windows `winget install --id GitHub.cli --accept-source-agreements --accept-package-agreements` (o Windows pede permissão: Sim). Login, que a própria pessoa faz: `gh auth login` → GitHub.com → HTTPS → "Authenticate Git with your GitHub credentials?" **Yes** → "Login with a web browser" (copiar o código de 8 letras e colar no navegador).
   - Python 3.11 ou mais novo: https://www.python.org/downloads/. O `python3` que vem no Mac é velho: depois de instalar, use `python3.12` (ou a versão instalada). No Windows, o mais seguro é `winget install --id Python.Python.3.12 -e --accept-source-agreements --accept-package-agreements` (pelo site, marcar "Add python.exe to PATH" se aparecer) e usar `py`. Na aba Code, depois de instalar com winget, feche e abra o app Claude antes do passo 6.
5. **Pegar o código** (depois do acesso):
   - **Procure um clone antes de clonar outro.** Mac: `find ~/Documents ~/Desktop ~/Downloads ~ -maxdepth 3 -type d -name PROJETO-TE-251 -not -path '*/Library/*' 2>/dev/null` · PowerShell: `Get-ChildItem $HOME\Documents,$HOME\Desktop,$HOME -Directory -Recurse -Depth 2 -Filter PROJETO-TE-251 -ErrorAction SilentlyContinue`.
   - Achou: entre nela e rode `git status -sb`. Tem mudanças locais? Não apague: `git switch -c wip/<nome>`, `git add -A`, `git commit -m "wip: mudanças locais de antes da atualização"` e `git push -u origin wip/<nome>` (se o git pedir nome e e-mail: `git config --global user.name "<nome>"` e `git config --global user.email "<e-mail do GitHub>"`). Depois `git fetch origin`, `git switch main`, `git pull`.
   - Não achou: clone na pasta em que a IA está trabalhando, se ela foi criada para o projeto; senão em Documentos (`cd ~/Documents`; PowerShell `cd $HOME\Documents`). Comando: `gh repo clone willianfabbrasil-a11y/PROJETO-TE-251` (sem `gh`: `git clone https://github.com/willianfabbrasil-a11y/PROJETO-TE-251`, com login pelo navegador). Anote o caminho completo do clone.
6. **Montar o contexto e seguir no projeto:**
   - Claude Code: abra na pasta do projeto (aba Code > escolher a pasta PROJETO-TE-251; no terminal, `cd PROJETO-TE-251` e depois `claude`, em duas linhas) e responda "Sim" para confiar na pasta. Ao abrir, ele carrega as regras e roda `equipe/sincronizar.sh` sozinho. Se a conversa continuar fora da pasta, rode `bash <caminho completo do clone>/equipe/sincronizar.sh`.
   - Outra IA com terminal: `bash equipe/sincronizar.sh` dentro da pasta (Windows: no Git Bash), **no começo de toda sessão**.
   - IA só de conversa: a cada sessão, a pessoa roda `bash equipe/sincronizar.sh` no terminal (Windows: Git Bash) dentro da pasta e cola a saída; no projeto do claude.ai, clica em Sincronizar no Conhecimento do projeto.
   - Leia nesta ordem: `AGENTS.md`, `equipe/PASSAGEM.md`, `equipe/NOVIDADES.md`, `equipe/frentes.yaml`, `equipe/estado/` e o fim de `equipe/DECISOES.md`. Mostre à pessoa um **resumo do projeto em até 8 linhas** (o que é, situação de hoje, frentes e o que cada uma exige, regras que mais pegam).
   - Siga a skill `entrar-no-projeto` (`.claude/skills/entrar-no-projeto/SKILL.md`; se a sua ferramenta não carrega skills, leia o arquivo e siga), levando o que já foi respondido aqui, sem perguntar de novo e sem repetir o resumo.

O app do projeto (instaladores Mac e Windows) fica nas Releases deste repositório público: https://github.com/willianfabbrasil-a11y/PROJETO-TE-251-instaladores/releases/latest
