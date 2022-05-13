# **Chave SSH**

&nbsp;

## **Criar a chave passos**

&nbsp;

    1. Inserir comando para gerar a chave:
        ssh-keygen -t ed25519 -C email
    2. Criar a senha
    3. Ir até o diretório que foi criado a chave
    4. Visualizar conteúdo da chave:
        cat id_ed25519.pub
    5. Copiar conteúdo e inserir no Github
    6. Inserir comando para criar agente:
        eval $(ssh-agent -s)
    7. "Entregar" a chave **Privada** para o agente (dentro da pasta em que foram geradas as chaves fica mais fácil):
        ssh-add id_ed25519
    8. Entrar com a senha

&nbsp;

## **Chave Token**

&nbsp;

    Gerado no Github
    Deve ser anotada e guardada no pc, pois não tera como visualizar novamente depois de criada
    Tem vida útil, posterior, deve ser criada nova chave
    Para copiar repositório, de vez utilizar link SSH, deve utilizar HTTPL