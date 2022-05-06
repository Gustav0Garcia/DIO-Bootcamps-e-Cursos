## Comandos básicos de Navegação 

TAB - Tem função de autocompletar
Seta para cima - navega pelo histórico do que foi digitado no terminal
Botão do meio do mouse - cola o que está copiado no CTRL+C

**ls** - Lista tudo que consta na pasta que você está
    ls -a - Lista arquivos ocultos também
**cd** - navegar pelas pastas
    cd / - move para a base do diretório
    cd /nome da pasta - para para a pasta desejada
    cd .. - volta 1 nível na pasta
**clear** - Limpa a tela do terminal 
    CTRL + L - atalho para limpar a tela

**mkdir** - cria pasta
**echo** - printa no terminal alguma frase que você escrever
    Exemplo
        echo Hello World
        echo hello > hello.txt - Verifica se consta algum arquivo com este nome, se não existir, ele ira criar
        echo > README.md - Cria arquivo
**rm** - deleta diretório
    Exemplo
        rm -rf workspace (flag -rf)
**pwd** - Mostra caminho em que está
**mv** - Move pastas
    mv teste.md ./pasta/

## Primeira vez utilizando Git

Deve ser feito configuração, fornecer e-mail e nick de autor (**Para facilitar, utilizar o mesmo do cadastro do GitHub**)
    git config --global user.email "email"
    git config --global user.name "name" 

## Comandos Git

**git clone** - Copia repositório
    git clone caminho_ssh_do_repositório_no_github  - (caso já esteja configurado chave SSH, ou utilizar HTTPL)
        Na primeira vez que estiver utilizando, irá pedir autorização (fingerprint)
**git init** - Inicia o Git
**git add** - Adiciona o que consta na pasta (tanto criação de arquivos, quanto modificações)
    git add teste.txt
    git add * - Adiciona tudo que tem na pasta
    git add . - Adiciona tudo que tem na pasta
**git commit -m** - Dá significado a todos os arquivos e modificações, juntamente colocando mensagem do que foi criado e/ou modificado
    git commit -m "mensagem" (-m é uma flag do git)
**git status** - Mostra os status dos arquivos, se está Untracked, Unmodiefied, Modiefied e Staged
**git config --list** - exibe listagem de todas as configurações do Git
    Caso queira alterar algo
        git config --global --unset *o_que_quer_alterar* (comando irá retirar as informações, deve ser inserida as novas informações depois)    
            Exemplo de alterar e-mail e name
                Retirar as informações
                git config --global --unset user.email
                git config --global --unset user.name

                Inserir as informações
                git config --global user.email "email"
                git config --global user.name "name"
    Commits já feitos no e-mail e autor anterior, não há como modificar, mas não irá causar prejuízo.
**git remote** - Colocar repositório local no remoto
    Deve criar o repositório no GitHub e copiar o caminho HTTPS para inserir (push) no Git
    Comando:
        git remote add origin link_do_repositório_pego_no_GitHub
    Listar repositórios cadastrados:
        git remote -v


## Colocar repositório local no remoto (Push)

Deve criar o repositório no GitHub e copiar o caminho HTTPS para inserir (push) no Git
Comando:
    git remote add origin link_do_repositório_pego_no_GitHub
Listar repositórios cadastrados:
    git remote -v