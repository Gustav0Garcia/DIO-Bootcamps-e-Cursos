## Chave SSH

# Criar a chave
    Inserir comando para gerar a chave:
        ssh-keygen -t ed25519 -C email
    Criar a senha
    Ir até o diretório que foi criado a chave
    Visualizar conteúdo da chave:
        cat id_ed25519.pub
    Copiar conteúdo e inserir no Github
    Inserir comando para criar agente:
        eval $(ssh-agent -s)
    "Entregar" a chave **Privada** para o agente (dentro da pasta em que foram geradas as chaves fica mais fácil):
        ssh-add id_ed25519
    Entrar com a senha


## Chave Token
    Gerado no Github
    Deve ser anotada e guardada no pc, pois não tera como visualizar novamente depois de criada
    Tem vida útil, posterior, deve ser criada nova chave
    Para copiar repositório, de vez utilizar link SSH, deve utilizar HTTPL