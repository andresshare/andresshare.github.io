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
  

# COSAS QUE NO SABIAS DE RUBY

En 2018, Ruby obtuvo el quinto lugar entre los 23 lenguajes de programación más buscados para aprender a continuación por los desarrolladores.
- **Ruby**  permite escribir un código limpio con un mínimo 'ruido' sintáctico y semántico, ofrece muchas bibliotecas para implementar una variedad de funcionalidades y admite aspectos como la programación orientada a objetos (OOP), la tipificación dinámica y la metaprogramación. ¿Porque es esto importante?


- **OOP** La mayoría de las entidades en Ruby, incluidos los literales lógicos, numéricos y de cadena, y algunas entidades elementales se pueden recrear como objetos y métodos. Este enfoque facilita el diseño de sistemas complejos y escalarlos sin duplicación de código.

- **Tipificación dinámica** En la tipificación dinámica, la validación de tipo se realiza durante la ejecución del programa y no durante la compilación. Esto permite a los desarrolladores de Ruby simplificar la escritura de pequeños scripts y macros. Pueden reutilizar variables, desarrollar marcos más flexibles y fáciles y crear aplicaciones de una manera más conveniente.


- **Metaprogramming** 
  permite crear código de software y bibliotecas que otros desarrolladores pueden reutilizar y personalizar fácilmente de acuerdo con las necesidades y tareas a resolver. Al entrar en la metaprogramación, los desarrolladores pueden crear DSL - Lenguajes específicos de dominio para resolver tareas complejas dentro de industrias específicas. DSL permite a los profesionales de alto nivel, como administradores de sistemas, trabajar y realizar cambios en el software.

- En el ecosistema de Ruby, los estándares de escritura y código de estructuración son aprobados por la comunidad global de desarrolladores y registrados en la guía de estilo de Ruby. (La guía de estilo de rieles también está aprobada). 

Un gran ejemplo de estandarización efectiva en Ruby: el mecanismo de creación de bibliotecas y herramientas llamado Gems (más de 140K de ellas disponibles). 

Todas las bibliotecas de Ruby tienen la misma estructura y se almacenan en un único repositorio: Ruby Gems. 

Esto determina la velocidad de obtención de las bibliotecas necesarias y la capacidad de navegar fácilmente por las nuevas herramientas. 

El ecosistema de Ruby ofrece un juego de herramientas completo para las pruebas (**RSpec, Capybara y Cucumber)**. Además, Ruby presta mucha atención a verificar cómo el código se ajusta a las normas y estándares **(RuboCop, SimpleCov, RubyCritic, Rails_best_practices)**.

**Ruby on Rails (RoR)** no es el único framework de Ruby, pero es el más popular y, por lo tanto, merece una atención especial. Rails ayudó a la gran cantidad de proyectos agradables a cobrar vida. 

Ruby on Rails se basa en la convención para escribir menos código y evitar la repetición. Este es el marco de código abierto, abierto y de uso gratuito, incluso con fines comerciales. La comunidad de Ruby ha creado soluciones útiles de código abierto, mediante las cuales los desarrolladores pueden crear fácilmente desde cero aplicaciones completamente funcionales que cumplan con los requisitos de seguridad y sean efectivas desde el punto de vista de los gastos, así como desde el punto de vista del desarrollo.

- **RAILS para startups.** Con Ruby on Rails, las startups pueden encontrar muchas respuestas a un problema que solo creen que podrían enfrentar. Es probable que encuentre cientos de elementos sobre un tema determinado. Todos los patrones o estructuras que puede desear ya existen, solo tiene que configurar algo, ¡y listo! Esto es genial para la creación rápida de prototipos. Un equipo pequeño puede obtener un producto viable mínimo en beta muy rápidamente utilizando herramientas con las que es divertido trabajar. En los EE. UU., Rails es el marco más buscado para las startups.

- **RAILS para empresas.** Cuando administra un gran negocio, la flexibilidad es una de las primeras prioridades. El truco está en la disponibilidad de los desarrolladores de Rails. El desarrollador que necesita está aquí antes que usted. Debido a que Ruby es elegante y fácil de comenzar, tiene un gran ecosistema y complementos para cada necesidad posible. A la nueva generación de programadores le encanta. Los desarrolladores pueden participar y comenzar a codificar de inmediato.

Usted puede usar

- [BonsaiERP](https://github.com/bonsaiERP/bonsaiERP) sistema ERP 
- [Fat Free CRM](http://www.fatfreecrm.com) sistema CRM
- [Discourse**](https://github.com/discourse/discourse) sistema de discucion 
- [Open Source Billing](https://github.com/vteams/open-source-billing) sistema de facturacion
-  [Spina CMS](https://www.spinacms.com/) administracion de contenido

### Ruby frameworks
 - [Ruby on Rails](https://rubyonrails.org/)
- [Sinatra](http://sinatrarb.com/) es orientado a servicios
- [Hanami](https://hanamirb.org/) una alternativa web app

### HERRAMIENTAS RUBY

### Testing

[RSpec](https://rspec.info/):BDD-framework;
[Capybara](https://github.com/teamcapybara/capybara) test de aceptacion para web aplications;
[Cucumber](https://github.com/cucumber/cucumber-ruby) BDD;
[Minitest](https://github.com/seattlerb/minitest) una libreria unit-tests, un analogo de RSpec
[Shoulda-matchers](https://github.com/thoughtbot/shoulda-matchers) mas metodos para  RSpec.
[Factory_bot](https://github.com/thoughtbot/factory_bot) — configurar objetos Ruby;
[Faker](https://github.com/faker-ruby/faker)  Crear test de datos;
[WebMock](https://github.com/bblimke/webmock) — establecer HTTP requests;
[Selenium WebDriver](https://rubygems.org/gems/selenium-webdriver/versions/2.53.4?locale=es) — Ruby bindings para WebDriver.

### Analisis de codigo

[RuboCop](https://github.com/rubocop-hq/rubocop) analizador de codigo Ruby;
[Simplecov](https://github.com/colszowka/simplecov) Analizador de codigo Ruby 1.9+;
[RubyCritic](https://github.com/whitesmith/rubycritic) un reportero de calidad de codigo;
[Rails_best_practices](https://github.com/flyerhzm/rails_best_practices) —una herramienta para verificar la calidad de codigo ruby


### Autorizacion


[Warden](https://github.com/wardencommunity/warden)  General Rack marco de  Autenticacion 
[Devise](https://makeitrealcamp.gitbook.io/ruby-on-rails-5/devise) Una  authentication  flexible para Rails;
[JWT](https://github.com/jwt/ruby-jwt) — JSON Web Token standard implemntado para Ruby;
[Doorkeeper](https://github.com/doorkeeper-gem/doorkeeper) Un OAuth2 para Rails;
[OAuth2](https://github.com/oauth-xx/oauth2) a Ruby wrapper para OAuth 2.0;
[CanCanCan](https://github.com/CanCanCommunity/cancancan) — Una continuacion de CanCan, para Ruby on Rails.;
[Pundit](https://github.com/varvet/pundit)  un CanCanCan ligera version de alternativa.

### Api


[ActiveModel::Serializers](https://github.com/rails-api/active_model_serializers) — JSON generation tool, para el Rails app;
[GraphQL-Ruby](https://github.com/rmosolgo/graphql-ruby) implementacion de Ruby para GraphQL
[Grape](https://github.com/ruby-grape/grape) un Micro-framework
[REST](https://code.tutsplus.com/es/articles/crafting-apis-with-rails--cms-27695)-Como APIs en Ruby;
[Apipie](https://github.com/Apipie/apipie-rails)  un administrador de documentacion API
[Swagger](https://swagger.io/tools/open-source/open-source-integrations/)  Un automatizado para crear Documentacion para Grape API.

### Abstraccion


[Dry-rb](https://dry-rb.org/) — Una variada libreria para tareas comunes, esto permite usar la programacion funcional ;
[Trailblazer](http://trailblazer.to/) — un marco que impone la encapsulación, una estructura de código intuitiva y le brinda una arquitectura orientada a objetos
[Interactor](https://github.com/collectiveidea/interactor) — permite la estructuración de la lógica de negocios.


### Assets

 [Asset_sync](https://github.com/AssetSync/asset_sync) Sincroniza Assets entre Rails y S3

[Autoprefixer](https://github.com/ai/autoprefixer-rails) herramienta para analizar Css y añadir vendor Prefixes

[CSS-props](https://w3c.github.io/i18n-drafts/articles/ruby/styling.en.html) - para una mejor experiencia entre navegadores.

### Cliente HTTP


[HTTParty](https://github.com/jnunemaker/httparty)
forma conveniente de trabajar con solicitudes HTTP;
[Faraday](https://github.com/lostisland/faraday) — una biblioteca de cliente HTTP que proporciona una interfaz común a través de muchos adaptadores y adopta el concepto de middleware Rack al procesar el ciclo de solicitud / respuesta;
[GraphQL-client](https://github.com/github/graphql-client) — una libreria para trabajar con solicitudes GraphQL.

### Desarrollo Movil

[RubyMotion](http://www.rubymotion.com/) — Le permite desarrollar y probar rápidamente aplicaciones nativas de iOS y OS X para iPhone, iPad, Mac y Android;
[Ruboto](http://ruboto.org/) — Una plataforma para desarrollar aplicaciones independientes completas para Android;

[Ruby Push Notifications](https://github.com/rpush/rpush) — iOS, Android y Windows Phone de notificaciones Push.


### Machine Learning

[Machine-learning-with-ruby](https://github.com/arbox/machine-learning-with-ruby) — Recursos en ruby.

### Inteligencia artificial
 [ai4r](https://github.com/SergioFierens/ai4r)
Un patio de juegos Ruby para investigadores de IA.

 > Ruby no es perfecto 


```
A pesar de la alta velocidad de desarrollo,Ruby no demuestra el mejor rendimiento. Por un lado, Ruby realiza muchas operaciones para la conveniencia del desarrollador, incluida la 
administración de memoria para la escritura dinámica. 
Por otro lado, por supuesto, el volumen de las operaciones afecta la velocidad de ejecución. 
Este criterio no es el más problemático, pero podría ser mejor. 
```


Ruby multithreading es lento. El algoritmo multihilo de Ruby es algo impredecible: puede cambiar de un hilo a otro en cualquier momento y es difícil de predecir o controlar. Esto afecta el resultado de procesar datos y realizar cambios y, en general, la velocidad de todo el proceso. En este momento, ```la comunidad Ruby está trabajando en este tema.```

Hasta la proxima!


recuerda puedes mirar esta guia de ruby

💎 [Ruby poder sin limites](https://soyandresbernal.github.io/ruby/2019/08/30/ruby-podersinlimites.html)