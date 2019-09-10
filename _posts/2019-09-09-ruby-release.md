---
layout: post
title:  "Ruby en su version 2.5.0"
date:   2019-09-9 19:08:10 +0530
categories: Ruby 💎
---

![.select en Ruby](https://media.giphy.com/media/AEAFLn3fOUImY/giphy.gif)


- Aumento del rendimiento del 5-10%, en  camino a los grandes aumentos de rendimiento prometidos para 3.0

- ahora `rescue/else/ensure` in do blocks 

- Nuevas capacidades de cobertura de prueba para métodos y ramas

#COSAS QUE NO SABIAS DE RUBY

- En 2018, Ruby obtuvo el quinto lugar entre los 23 lenguajes de programación más buscados para aprender a continuación por los desarrolladores.
- Ruby le permite escribir un código limpio con un mínimo 'ruido' sintáctico y semántico, ofrece muchas bibliotecas para implementar una variedad de funcionalidades y admite aspectos como la programación orientada a objetos (OOP), la tipificación dinámica y la metaprogramación. ¿Porque es esto importante?


- **OOP** La mayoría de las entidades en Ruby, incluidos los literales lógicos, numéricos y de cadena, y algunas entidades elementales se pueden recrear como objetos y métodos. Este enfoque facilita el diseño de sistemas complejos y escalarlos sin duplicación de código.

- **Tipificación dinámica** En la tipificación dinámica, la validación de tipo se realiza durante la ejecución del programa y no durante la compilación. Esto permite a los desarrolladores de Ruby simplificar la escritura de pequeños scripts y macros. Pueden reutilizar variables, desarrollar marcos más flexibles y fáciles y crear aplicaciones de una manera más conveniente.


- **Metaprogramming** 
  permite crear código de software y bibliotecas que otros desarrolladores pueden reutilizar y personalizar fácilmente de acuerdo con las necesidades y tareas a resolver. Al entrar en la metaprogramación, los desarrolladores pueden crear DSL - Lenguajes específicos de dominio para resolver tareas complejas dentro de industrias específicas. DSL permite a los profesionales de alto nivel, como administradores de sistemas, trabajar y realizar cambios en el software.

- En el ecosistema de Ruby, los estándares de escritura y código de estructuración son aprobados por la comunidad global de desarrolladores y registrados en la guía de estilo de Ruby. (La guía de estilo de rieles también está aprobada). 

Un gran ejemplo de estandarización efectiva en Ruby: el mecanismo de creación de bibliotecas y herramientas llamado Gems (más de 140K de ellas disponibles). Todas las bibliotecas de Ruby tienen la misma estructura y se almacenan en un único repositorio: Ruby Gems. Esto determina la velocidad de obtención de las bibliotecas necesarias y la capacidad de navegar fácilmente por las nuevas herramientas. El ecosistema de Ruby ofrece un juego de herramientas completo para las pruebas (RSpec, Capybara y Cucumber). Además, Ruby presta mucha atención a verificar cómo el código se ajusta a las normas y estándares (RuboCop, SimpleCov, RubyCritic, Rails_best_practices).

- Ruby on Rails (RoR) no es el único marco de Ruby, pero es el más popular y, por lo tanto, merece una atención especial. Rails ayudó a la gran cantidad de proyectos agradables a cobrar vida. Ruby on Rails se basa en la convención para escribir menos código y evitar la repetición. Este es el marco de código abierto, abierto y de uso gratuito, incluso con fines comerciales. La comunidad de Ruby ha creado soluciones útiles de código abierto, mediante las cuales los desarrolladores pueden crear fácilmente desde cero aplicaciones completamente funcionales que cumplan con los requisitos de seguridad y sean efectivas desde el punto de vista de los gastos, así como desde el punto de vista del desarrollo.

- **RAIlS para startups.** Con Ruby on Rails, las startups pueden encontrar muchas respuestas a un problema que solo creen que podrían enfrentar. Es probable que encuentre cientos de elementos sobre un tema determinado. Todos los patrones o estructuras que puede desear ya existen, solo tiene que configurar algo, ¡y listo! Esto es genial para la creación rápida de prototipos. Un equipo pequeño puede obtener un producto viable mínimo en beta muy rápidamente utilizando herramientas con las que es divertido trabajar. En los EE. UU., Rails es el marco más buscado para las startups.

- **RAILS para empresas.** Cuando administra un gran negocio, la flexibilidad es una de las primeras prioridades. El truco está en la disponibilidad de los desarrolladores de Rails. El desarrollador que necesita está aquí antes que usted. Debido a que Ruby es elegante y fácil de comenzar, tiene un gran ecosistema y complementos para cada necesidad posible. A la nueva generación de programadores le encanta. Los desarrolladores pueden participar y comenzar a codificar de inmediato.

puede usar
- **bonsaiERP** para sistemas ERP 
- **Fat Free CRM** sistemas CRM
-  **Discourse** sistema de discucion 
- **Open Source Billing** sistema de facturacion
-  **Spina CMS** administracion de contenido

Ruby frameworks
- **Ruby on Rails**
- **Sinatra** es orientado a servicios
- **Hanami** una alternativa web app

### HERRAMIENTAS RUBY

**Testing**

**RSpec**:BDD-framework;
**Capybara** — acceptance test framework for web applications;
**Cucumber** — BDD that talks to domain experts first and code second;
**Minitest** — a library for unit-tests, a simpler analog of RSpec;
**Shoulda-matchers** — additional matcher-methods for RSpec.
**Factory_bot** — for setting up Ruby objects as test data;
**Faker** — a library for creating test data;
**WebMock** — for stubbing and setting expectations on HTTP requests;
**Selenium WebDriver** — Ruby bindings for WebDriver.

Analisis de codigo

Code analysis

**RuboCop** — a static code analyzer, based on the community Ruby style guide;
**Simplecov** — Code coverage for Ruby 1.9+;
**RubyCritic** — a Ruby code quality reporter;
**Rails_best_practices** — a tool to check Ruby code quality.


### AUTORIZACION


**Warden** — General Rack Authentication Framework;
**Devise** — a flexible authentication solution for Rails based on Warden;
**JWT** — JSON Web Token standard implementation for Ruby;
Doorkeeper — an OAuth2 provider for Rails;
**OAuth2** — a Ruby wrapper for the OAuth 2.0 protocol;
**CanCanCan** — continuation of CanCan, an authorization Gem for Ruby on Rails.;
**Pundit** — CanCanCan lightweight alternative.

**API**


**ActiveModel::Serializers** — JSON generation tool for the Rails app;
**GraphQL-Ruby** — Ruby implementation of GraphQL;
**Grape** — a micro-framework for creating **REST**-like APIs in Ruby;
**Apipie** — documentation management API;
**Swagger** — this gem provides an autogenerated documentation for your Grape API.

### Abstraccion


**Dry-rb** — a collection of Ruby libraries intended to encapsulate a common task, it allows you to program in Ruby in functional programming style;
**Trailblazer** — a framework that enforces encapsulation, an intuitive code structure and gives you an object-oriented architecture;
**Interactor** — allows business-logic structuring.


### Assets

**Sass and Less** — leaner CSS assets;

**Asset_sync** — synchronizes Assets between Rails and S3

**Autoprefixer** — automatically adds 

**CSS-props** for a better cross-browser experience.

### Cliente HTTP


**HTTParty** — convenient way to work with HTTP-requests;
**Faraday** — an HTTP client library that provides a common interface over many adapters and embraces the concept of Rack middleware when processing the request/response cycle;
**GraphQL-client** — a lib to work with GraphQL requests.

Desarrollo Movil

Mobile development


**RubyMotion** — a toolchain that lets you quickly develop and test full-fledged native iOS and OS X applications for iPhone, iPad, Mac, and Android;
**Ruboto** — a platform for developing full stand-alone apps for Android;
**Ruby Push Notifications** — iOS, Android and Windows Phone Push notifications.


### MACHINE LEARNING

**Machine-learning-with-ruby** — resources for machine learning in Ruby.

### INTELIGENCIA ARTIFICIAL
 **ai4r** — A Ruby playground for AI researchers.

 Ruby no es perfecto 

   A pesar de la alta velocidad de desarrollo,Ruby no demuestra el mejor rendimiento. Por un lado, Ruby realiza muchas operaciones para la conveniencia del desarrollador, incluida la administración de memoria para la escritura dinámica. Por otro lado, por supuesto, el volumen de tales operaciones afecta la velocidad de ejecución. Este criterio no es el más problemático, pero podría ser mejor.


Ruby multithreading es lento. El algoritmo multihilo de Ruby es algo impredecible: puede cambiar de un hilo a otro en cualquier momento y es difícil de predecir o controlar. Esto afecta el resultado de procesar datos y realizar cambios y, en general, la velocidad de todo el proceso. En este momento, la comunidad Ruby está trabajando en este tema.

