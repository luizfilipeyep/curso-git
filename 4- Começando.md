# 4- Começando

###### 01/03/2022



## Iniciando um repositório
Nesta aula iremos iniciar um repositório, primeiramente iremos criar um novo diretório, em seguida navegaremos até nosso diretório recém criado através do terminal.

Após selecionarmos essa pasta, iremos rodar o comando `git init`, e assim que for executado, o nosso repositório será criado.

Você pode notar que aparentemente nada foi adicionado no diretório, mas caso rode o comando `ls -a`, verá que aparece uma pasta .git, que é justamente o que queríamos.



## O git guarda o histórico do projeto
Nesta aula, veremos onde o git guarda o histórico do nosso projeto, todos os detalhes e arquivos, tudo que estamos fazendo dentro do projeto.

------



Apenas rode o comando a seguir:

```
ls -al .git
```

Verá que há alguns arquivos nessa pasta, e são exatamente esses arquivos que nos trazem as informações do Git.

Atenção: Nunca delete a pasta git caso não esteja na nuvem, ela é seu repositório, no caso de você deletá-la, perderá todo o histórico do seu projeto.



## O primeiro commit
Nesta aula iremos criar nosso primeiro commit, nosso primeiro ponto na história.

------



Primeiro iremos preparar nosso arquivo para isso, através do comando add, usado da seguinte forma:

```
git add .
```

O . nesse caso serve para selecionarmos todos os arquivos dentro do diretório.

Assim que tivermos executado esse comando, podemos criar nosso commit, da seguinte forma:

```
git commit -m "mensagem do commit, é obrigatória, então não se esqueça!"
```

E assim criamos nosso primeiro ponto na história!



## Git log
Assim que rodar o comando no seu projeto, verá que temos uma hash, do tipo SHA-1, e também teremos entre parênteses o nosso branch, nesse caso o master, e no commit (sua hash), teremos o autor do commit, a data do mesmo e a mensagem do commit.

Caso queiramos um resultado menor desse comando, podemos usar a opção --oneline, da seguinte forma:

```
git log --oneline
```

Ele vai encurtar a hash, retirar o autor, a data e exibir a mensagem do commit ao lado.

Suponhamos que você tem 50 commits, e precisa apenas dos últimos 5, nesse caso, rode o comando a seguir:

```
git log -n 5
```

Ou seja, apenas coloque o argumento -n e a quantidade dos últimos commits que deseja.

Caso queira ver os commits após uma data específica, utilize o argumento --since, da seguinte forma:

```
git log --since=aaaa-mm-dd
```

Já caso queira os commits antes de uma data específica, use o argumento --until, da seguinte forma:

```
git log --until=aaaa-mm-dd
```

Você também pode aplicar um filtro para o autor do commit, para procurar os commits de uma pessoa em específico, usando o argumento --author, utilizado da seguinte forma:

```
git log --author=nomedoautor(nao precisa ser completo)
```

Também temos a forma mais poderosa de se utilizar o git log que é com o argumento grep, usado da seguinte forma:

```
git log --grep="o que quer que esteja buscando, ex: bugfix"
```

Basicamente significa expressão regular global, é muito comum na programação, e vai ser usado para buscar na mensagem do commit o que quer que você esteja buscando.