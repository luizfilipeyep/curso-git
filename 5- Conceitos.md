# 5- Conceitos

###### 02/03/2022



## Estágios do arquivo

Veremos nesta aula sobre os três estados dos arquivos dentro do git.

Para podermos iniciar um projeto, colocamos o git init (ou git clone, caso queiramos copiar os arquivos de outro repositório, mas veremos isso mais adiante), após isso, o git vai iniciar um repositório local, fazendo com que nosso arquivos fiquem no Working Directory, a primeira etapa do processo.
Após isso, faremos o git add, que nos coloca na Stage Area, a segunda etapa do processo, e finalmente faremos um commit, para levar nossos arquivos até o repositório local.

O working Directory é o diretório no qual se encontra nosso projeto, então os arquivos são preparados para serem commitados, a Stage Area, onde nosso arquivos ficam preparados, para podermos enfim criarmos o nosso commit, e é a partir desse ponto em que nosso arquivo fica salvo como um ponto na história.

Não se preocupe se ficou confuso, faremos na prática ainda nas próximas aulas, certo?



## Git Workflow

Nessa aula falaremos sobre como funciona o workflow do git, que vimos na aula passada, onde criamos o primeiro arquivo, passamos pela stage area, e adicionamos ao repositório.

Primeiramente suponhamos que temos um arquivo, e nós o preparamos através do git add. Isso significa que ele teve uma cópia de si feita, e essa cópia foi enviada para a nossa stage area, então temos dois arquivos, onde podemos trabalhar em nosso working directory, enquanto nossa versão no stage area continua a mesma, podendo ter duas versões diferentes do nosso arquivo.

Podemos então colocar ele no nosso repositório local, através do comando git commit, onde criamos um ponto na história, onde temos nosso arquivo naquele momento do tempo.

Agora faremos uma alteração nesse arquivo, e teremos então o arquivo (v2), e faremos o mesmo processo para ele, passando para o stage area, e iniciando um commit, então no nosso repositório teremos a v1 e a v2, a v2 ficando por último, visto que é uma linha do tempo, então podemos criar a v3 e fazer o mesmo processo, criar a v4 e repetir, e nós teremos todas as versões do nosso arquivo salvas dentro do nosso repositório.

Podemos voltar atrás em todas as versões dos arquivos, porém a numeração não será bonitinha, teremos que usar a hash, sobre a qual falaremos na próxima aula.



## Hash SHA-1

Nessa aula, falaremos sobre o nome dado à cada commit, que é dado através de uma hash chamada SHA-1.

A cada commit que criamos, o git vai gerar um checksum, que converte os dados da nossa operação em um número, o que garante a integridade dos nossos dados. Essa hash é uma linha de 40 caracteres hexadecimais.

Dentro dessa string existe uma snapshot, que mostra o autor, o pai e a mensagem do nosso commit.

O pai do commit é o commit do qual ele foi criado, então o nosso primeiro commit sempre terá um valor nulo, enquanto os próximos terão o valor do commit anterior a ele.



## HEAD

No git, a HEAD é um ponteiro, que nos aponta em que ponto da história estamos, em qual commit nós estamos, e nas próximas aulas veremos como fazer para irmos em outros pontos na história, outros commits.

(Não é necessário entender as minúcias de como o git funciona, precisamos entender como funciona, não todos os detalhes exatos de todo o funcionamento do git. Nosso foco tem de ser em como fazê-lo uma ferramenta da qual possamos usar no nosso dia-a-dia, certo?).