---
layout: post
title: "Programação em Scripts - Segunda Entrega"
published: true
---

**Aula 01 - Virtualenv em Unix**


O vídeo demonstra a instalação da biblioteca Python Virtualenv que requer a versão 2.7 do Python. A instalação pode ser feita das seguintes formas:


   * Instalar diretamente com o gerenciador de pacotes apt-get (Linux) - apt-get install python-virtualenv;

   * Instalar com o gerenciador de pacotes brew (Mac) - brew install virtualenv e em seguida instalar com o instalador de pacotes Python pip - pip install virtualenv; 




**Aula 02 - Tekton no Linux**

Este vídeo demonstra a instalação do framework Tekton juntamente com a instalação do Google AppEngine. Alguns passos destacados foram:



   * Adicionar o diretório do Google AppEngine ao PATH por meio do arquivo .bashrc após instalação do Google AppEngine e criar variável GAE_SDK para o Tekton;
   * Obter o Tekton via Github;
   * Instalar as bibliotecas requeridas pelo Teton por meio da execução do script venv.sh (Linux e Mac);
   * Iniciar o servidor local do Google AppEngine por meio do dev_appserver.py para o projeto Tekton.





**Aula 03 - Pycharm e Linux**


O vídeo demonstra a instalação do IDE (IDE, do inglês Integrated Development Enviroment) Pycharm. Os passos destacados são:


   * Importar o projeto Tekton obtido conforme o vídeo anterior;
   * Configurar a IDE para utilizar o ambiente virtual e suas bibliotecas criadas pelo Virtualenv;
   * Configurar o servidor do Google AppEngine para o projeto Tekton;
   * Configurar as pastas de código-fonte para auto-complete da IDE entre outras funções;





**Questões - Capitulo**1



**1. Quais as duas principais versões atuais do interpretador Python?**
São as versões 2.7 e 3.4.


**2. Qual versão de Python é suportada atualmente pelo App Engine**?
A versão 2.7 é a atualmente suportada.

**3. Para que serve o SDK do App Engine?**
Fornece as ferramentas necessárias para inicializar o servidor localmente, interagir com o banco de dados e etc.


**4. Qual a vantagem de colocar  ferramentas instaladas no path do Sistema Operacional?** 
Dessa forma o acesso a tais ferramentas fica mais fácil para o usuário e outros programas.


**5.O que é e para que serve uma IDE?**
Ambiente Integrado de Desenvolvimento (Integrated Development Environment) é um conjunto de ferramentas integradas a fim de facilitar a atividade de desenvolvimento.


**6. Como se chama o arquivo de configuração de uma aplicação App Engi**ne?
O arquivo se chama app.yaml.


**7. Qual o domínio padrão para acessar aplicações App Engine na internet?**
appspot.com



**Questões - Capitulo 2**


**1. Qual o nome do arquivo de configuração do Google App Engine?**
    app.yaml

**2. Para que serve o item application do arquivo de configuração?**
    O application serve para identificar a aplicação.

**3. Para que serve o item version do arquivo de configuração?**
    Indica qual é a versão da aplicação.

**4. Qual endereço deve ser utilizado para acessar uma aplicação com id foo e versão 35?**
    35.foo.appspot.com ou 35-dot-foo.appspot.com

**5. Para que serve a seção libraries do arquivo de configuração?**
    Define as bibliotecas necessárias

**6. Para que serve a seção handlers do arquivo de configuração?**
    Define qual código a ser executado de acordo com a url da requisição.

**7. Como são definidos os paths mapeados no arquivo de configuração?**
    Com expressões regulares.

**8. Por que é necessário mapear RequestHandlers nos scripts Python?**
    Para permitir a definição de várias classes em um único arquivo.

**9. Para que serve a classe RequestHandler?**
    Para definir qual classe irá tratar de uma requisição HTTP.

**10. Como se relacionam os métodos da classe RequestHandler e os do protocolo HTTP?**
    Os métodos da RequestHandler servem para processar as requisições HTTP.

**11. Para que serve o objeto Request?**
    Para ter acesso as informações e parâmetros enviados por uma requisição HTTP.

**12. Como se obtém os valores de parâmetros enviados via query string em uma chamada HTTP do tipo GET?**
    Por meio do método self.request.get('<nome do parametro>’).

**13. Para que serve o objeto Response?**
    Serve para o envio de dados.

**14. Qual o método do objeto Response serve para enviar strings?**
    É o método se;f.response.write()

**15. Como é possível enviar uma resposta para redirecionamento?**
    Utilizando o método redirect da classe RequestHandler passando a url desejada como parametro para o redirecionamento.


**Questões - Capítulo 3**


**1. Para que serve o Virtualenv?**
Virtualenv permite que se crie um ambiente de dependências isolado para cada projeto.
  
**2. Qual a função do arquivo convention.py?**
Tratar as requisições HTTP POST, GET e PUT..
  
**3. Por que é necessário incluir bibliotecas através de código no arquivo convention.py?**
Porque o GoogleAppEngine não consegue instalar as bibliotecas por meio do virtualend ou o pip.
  
**4. Como ficaria a declaração de uma função para tratar a execução de chamada no path /usuario/salvar?nome=Renzo&idade=31?**
Criar o método def salvar(nome, idade) em usuario.py.

**5. Como se diferenciam parâmetros recebidos por injeção de dependência dos recebidos via requisição HTTP?**
Se diferenciam por conter um “_” antecedendo o nome da variável (Ex: _rest, _handler)
  
**6. Qual deve ser a posição de parâmetros recebidos via injeção de dependência?**
Devem ser os primeiros a serem declarados seguidos pelos demais parâmetros.
  
**7. Qual deve ser o parâmetro declarado quando for necessário fazer um redirecionamento?**
_handler
  
**8. Qual o script e função devem ser utilizados para se calcular paths com base em uma função?**
Deve ser usado o script router.py com base na função to_path().