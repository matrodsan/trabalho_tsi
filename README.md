<h1 align="center">
    <img src="https://upload.wikimedia.org/wikipedia/commons/f/f3/Instituto_Federal_do_Esp%C3%ADrito_Santo_-_Marca_Vertical_2015.svg" width="150px"/><br>
    Trabalho Colaborativo e Mídias Digitais
</h1>
<p align="center">
    Repositório para desenvolvimento da atividade de Trabalho Colaborativo e Mídias Digitais
</p>
<br>

## 1. Enunciado

Neste trabalho, o enunciado diz que cada integrante do grupo deverá realizar as seguintes tarefas:
1. Instalar o Git em sua máquina local
2. Fazer uma conta pessoal no Github
3. Configurar seu acesso ao Github via linha de comando com chaves SSH
4. Após isso, um dos integrantes do grupo irá criar um repositório público em seu perfil do Github, inserindo os usuários de seus demais colegas do grupo de trabalho como colaboradores, para que tenham acesso e possam enviar dados de suas máquinas locais para o repositório remoto. 
5. O criador do repositório irá colocar o seu nome completo em um arquivo chamado grupo.txt no repositório remoto. Cada um dos demais integrantes do grupo (colaboradores do repositório remoto) deverá clonar este repositório em sua máquina local, buscar os dados/arquivos do repositório remoto, inserir seu nome completo ao fim do arquivo grupo.txt que já havia sido criado pelo dono do repositório (nomes em sequência, um em cada linha), fazer commit/consolidar no repositório local e depois enviar de volta para o repositório remoto.
6. Os repositórios deverão ser públicos desde o início, para que os professores mediadores possam acompanhar a execução e o término da tarefa. As atualizações não devem ser feitas na interface web do repositório remoto, e sim via linha de comando em sua máquina local. Temos como verificar :-D
7. Cada integrante do grupo deverá enviar na tarefa o link para o repositório remoto do grupo e o nome do seu usuário no Github.
8. Cada um dos passos solicitados tem explicação nos livros semanais. Você deve sempre tentar reproduzir os tutoriais em vídeo na sua máquina.
9. O trabalho vale 12 pontos. Em caso de dúvidas, utilize o fórum e procure seu mediador.

## 2. Desenvolvimento
### 2.1 Instalação do Git
A instalação do Git pode ser feita de diferentes modos. No entando, vamos apresentar duas formas que se mostraram mais simples e eficazes de serem executadas para o nosso grupo.

A primeira forma, mais convencional, pode ser realizada acessando o site oficial do [Git](https://git-scm.com/) e realizando o download da ferramenta diretamente da plataforma, bastando somente executar o arquivo baixado e realizar a instalação do software.

A segunda maneira pode ser realizada através da linha de comando. Como explicado pelo professor Silvio no livro **Usando o Git**, podemos consultar diferentes gerenciadores de pacotes para realizar a instalação. Iremos apresentar a instalação do Git via linha de comando utilizando dois gerenciadores de pacote.

Debian-like (Ubuntu)
```
sudo apt install git
```

Winget (Windows)
```
winget install --id Git.Git -e --source winget
```

### 2.2 Fazer uma conta pessoal no Github
Criamos as contas no GitHub normalmente, utilizando a própria plataforma. Os usuários são:
- Ailson Ferreira de Sousa - [Ailson-de-Sousa](https://github.com/Ailson-de-Sousa)
- Brayham Procopio de Carvalho - [Brayham-Carvalho](https://github.com/Brayham-Carvalho)
- Marcelo da Silva Gomes - [marcelogomes22](https://github.com/marcelogomes22)
- Mateus Rodrigues Santos - [matrodsan](https://github.com/matrodsan)
- Pedro Rodrigues Santos - [PRSantos10](https://github.com/PRSantos10)
- Wanderson Barbosa da Silva - [wbsplus](https://github.com/wbsplus)

### 2.3 Configurar o acesso ao Github via linha de comando com chaves SSH
Para esse propósito utilizamos o próprio software já embutindo na instalação do Git através do seguinte modelo de linha de comando:
```
ssh-keygen -t ed25519 -C "seu_email@exemplo.com"
```
Vale ressaltar que esse tipo de chave é criptografado através do modelo da curva de Edwards. Como se trata de um tipo de criptografia moderna que foi desenvolvida recentemente, foi instruído que, caso houvesse algum problema de compatibilidade por conta da versão do ssh-keygen, usássemos a chave do tipo rsa através do modelo da linha de comando que segue:
```
ssh-keygen -t rsa -b 4096 -C "seu_email@exemplo.com"
```
Após configurar 

Após a criação das chaves, foi necessário informar uma senha de proteção para essas chaves.

Outra configuração impotante do Git é a informação do autor. Para isso, usamos:
```
git config --global user.name "Nome do Usuário"
git config --global user.email "seu_email@exemplo.com"
```

### 2.4 Configuração do repositório
O repositório remoto foi criado e configurado por mim ([matrodsan](https://github.com/matrodsan)), contendo um arquivo "***README.md***" com a informação inicial do repositório. A chave foi inserida para receber informações do Git devidamente e as contas adicionadas ao repositório são as mesmas contidas na [Seção 2.2](#22-fazer-uma-conta-pessoal-no-github).

### 2.5 Commit
Nessa etapa do trabalho tínhamos a tarefa de realizar os commits, mais precisamente, cada integrante do grupo. Dessa forma, utilizamos a linha de comando para cumprirmos essa tarefa e o primeiro código utilizado para isso foi:
```
git clone git@github.com:matrodsan/trabalho_tsi.git
```
Em seguida, inserimos as informações solicitadas pelo enunciado no arquivo ***grupo.txt*** e usamos os códigos descritos abaixo para passar o arquivo do status _modified_ para _staged_. Por fim, realizamos o _commmit_ e o _push_ do projeto para realizar a consolidação do mesmo.

```
git add *
git commit -m "Comentário"
git push
```