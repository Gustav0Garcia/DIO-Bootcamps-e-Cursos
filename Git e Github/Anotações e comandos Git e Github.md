# **Tópicos fundamentais para entender o funcionamento do Git**

&nbsp;

## **SHA1**

A sigla **SHA** significa *Secure Hash Algorithm* (Algoritmo de Hash Seguro), é um conjunto de funções hash criptográficas projetadas pela **NSA** (Agência de Seguraça Nacional dos EUA).

A encriptação gera conjunto de characteres identificador de 40 dígitos. (são characteres de 40 dígitos únicos)

Exemplo no terminal:

    openssl sha1 texto.txt

&nbsp;

## **Objetos Internos do Git**

&nbsp;

**Blob** - Arquivos ficam guardados dentro do blob, e nele contem metadados.

    Guarda o **SHA1** do arquivo
    Vai ter dentro do Blob:
        1. Tipo do objeto
        2. Tamanho da string ou do arquivo
        3. Vai contem "\0" dentro
        4. conteúdo de fato do arquivo

**Tree** - Armazenam **Blobs** e apontam para tipos de **Blobs**, **Commits** e **Trees* diferentes.

    Também contém metadados.
    A Tree guarda o nome dos arquivos.
    Vai ser responsável por montar toda a estrutura de onde estão localizados os arquivos.
    Contém SHA1 dos metadados das Trees

**Commit** - Vai juntar tudo, ele aponta para uma **Tree**, para o último **Commit** realizado antes dele, para o **Autor** e para a **Mensagem** deixada quando faz o **Commit**.

    Commit da sentido/explicando todos os arquivos e pastas.
    Tem Time Stamp de quando foi criado.
    Também possuem um SHA1 de seus metadados.
    Aumenta credibilidade de que não houve alterações maliciosas de forma externa.
    É único para cada Autor

&nbsp;

## **Sistema Distribuido Seguro**

&nbsp;

É a versão remota mais recente, mais atualizado do seu código e com diversas pessoas contribuindo e tendo o seu código em suas máquinas.