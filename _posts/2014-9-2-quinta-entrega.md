---
layout: post
title: "Programação em Scripts - Quinta Entrega"
published: true
---

Nesta 5º entrega foram abordados os seguintes temas:

**Aula 11 - Login com Google - App Engine e Python**

Este video aborda o método de login usando o sistema de autenticação do Google e que já vem configurado no 
framework Tekton, além dos outros dois métodos possíveis de ser utilizado.

**Aula 11.1 - Login sem Senha com Passwordless - App Engine e Python**

Demonstração de como configurar o método de autenticação sem senha (necessita somente email) por meio do framework [passwordless](https://pswdless.appspot.com). Por meio
do site você receberá um id e um token de aplicação que deverá ser configurado na área administrativa do framework Tekton. Assim será possível
um usuário acessar o site sem a necessidade de senha, recebendo via email somente um url para validação por meio do passwordless.

**Aula 11.2 - Login com Facebook - App Engine e Pytho**

Desta vez, o detalhamento feito é sobre o método de autenticação por meio do Facebook. Igual ao passwordless é necessário
obter um id e um token para adicionar na área administrativa do tekton. A criação deste token é feito por meio do área voltada para desenvolvedores no Facebook: [developers.facebook.com](https://developers.facebook.com/). Aqui ddeve ser criada uma aplicação Web onde também é solicitado o domínio do site onde o sistema de autenticação será utilizado, feito isto o id e o token são gerados e devem ser cadastrados na área administrativa do tekton. Pronto!

**Aula 12 - Segurança - CSRF - App Engine e Python**

Por padrão o Tekton define que todo recurso deve estar seguro por padrão, a esta funcionalidade é dada o nome de White List. Caso não seja necessário a autenticação do usuáriom deve ser informada explicitamente o desejo para tal ação que é o que caracteriza o Cross Site Request Forgery - CSRF. 

Para evitar que parâmetros sejam enviados diretamente na URL deve ser criado um token aleatóriamente que deve ser acrescentado a uma form no seu envio e por meio de uma cookie feita a conferência.

**Aula 12.1 - Segurança - Permissões - App Engine e Python (continuação Aula 12)**

Neste vídeo é abordado o uso do decorator para a definição de permissões à diferentes áreas do site. Com "@login_not_required" define-se que determinada área não irá pedir a autenticação do usuário. Com o decorator @permissions() a restrição é feita somente a quem não pertence ao grupo especificado como parâmetro, sendo os grupos definidos em permission_app/model.py.
