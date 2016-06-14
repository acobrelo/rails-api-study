# Rails as an API Study

Use your favorite search engine and the provided readings to research and answer
the following questions (no prior knowledge is expected).

In your answers, be sure to cite any relevant sources you consulted in your
search. We ask you to write answers in your own words in order to see how you
process what you've read. Please do not answer with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

Please note:

-   Many of the readings will mention the "view" layer. We won't be covering the
    view layer in this program.
-   We'll use our [rails-api-template](/ga-wdi-boston/rails-api-template)
    repository as the basis for our rails applications.
    This template excludes the "view" layer.

## Required Readings

-   [Starting Ruby on Rails: What I Wish I Knew | BetterExplained](http://betterexplained.com/articles/starting-ruby-on-rails-what-i-wish-i-knew/)
-   [Intermediate Rails: Understanding Models, Views and Controllers | BetterExplained](http://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/)
-   [Getting Started with Rails — Ruby on Rails Guides](http://guides.rubyonrails.org/getting_started.html)
-   [The Rails Command Line — Ruby on Rails Guides](http://guides.rubyonrails.org/command_line.html)
-   [Rails Routing from the Outside In — Ruby on Rails Guides](http://guides.rubyonrails.org/routing.html)
-   [Action Controller Overview — Ruby on Rails Guides](http://guides.rubyonrails.org/action_controller_overview.html)

## Define Model Responsiblities

In your own words, define what the responsibilities of the model layer are in
Rails.

```md
Models, according to all sources, are what do the heavy lifting in Rails
and are the most logic-intensive. Each table of data requires a model and
models define the qualities of the data as well as how the data tables communicate
if at all. Basically, the model layer stores all relevant information about
how data should behave.
```

## Define Controller Responsiblities

In your own words, define what the responsibilities of the controller layer are
in Rails.

```md
The controller layer is responsible for receiving specific requests and for
communicating with the model layer {as well as view, though less relevant here}.
The controller is the first bastion that receives information and from there
communicates with the model and view layers independently. The controller receives
a given request and then determines where to look for data, gets data, then is
responsible for sending information back as a response.

```

## Define Router Responsiblities

In your own words, define what the router does in Rails.

```md
Routers are what serve as the communication between the URL and the controller
and also handle communication coming out of the controller all the way back to the
browser. When a request is received, the URL and the HTTP verb are basically
translated by the router so the appropriate controller action can be taken.
```

## The Request-Response Cycle in Rails

Starting with a client making a GET request to a particular URL, describe how
the parts of Rails interact to produce and send a response.

```md
An incoming request is first handled by the router so that the appropriate path
is created. Then, the controller action takes the path, determines what models
are going to be needed, and then is passed to the model layer. The model layer
executes the commands, finds the data, does the necessary task, and then passes
a response back to the controller layer, which in turn is passed to the router.
All components are updated accordingly and in communication with each other to
ensure that a request is handled properly, efficiently, and that the response
makes sense given the request.
```
