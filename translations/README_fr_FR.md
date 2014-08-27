# Martini  [![wercker status](https://app.wercker.com/status/9b7dbc6e2654b604cd694d191c3d5487/s/master "wercker status")](https://app.wercker.com/project/bykey/9b7dbc6e2654b604cd694d191c3d5487)[![GoDoc](https://godoc.org/github.com/go-martini/martini?status.png)](http://godoc.org/github.com/go-martini/martini)

Martini est excellent package pour écrire rapidement des applications ou services web en Golang.

## Pour commencer
Après avoir intallé GO et défini votre [GOPATH](http://golang.org/doc/code.html#GOPATH), créer votre premier fichier `.go`. Nous l'appellerons `server.go`.

~~~ go
package main

import "github.com/go-martini/martini"

func main() {
  m := martini.Classic()
  m.Get("/", func() string {
    return "Hello world!"
  })
  m.Run()
}
~~~

Ensuite installez le paquet martini (**go 1.1** ou supérieur est requis):

~~~
go get github.com/go-martini/martini
~~~

Ensuite éxecutez votre serveur:

~~~
go run server.go
~~~

Vous avez maintenant un serveur web Martini qui fonctionne sur `localhost:3000`

## Besoins d'aide

Rejoignez nous sur la [list de diffusion](https://groups.google.com/forum/#!forum/martini-go)

Regardez la [Vidéo de démonstration](http://martini.codegangsta.io/#demo)

Posez des questions sur Stackoverflow en utilisant le [tag martini](http://stackoverflow.com/questions/tagged/martini)

GoDoc [documentation](http://godoc.org/github.com/go-martini/martini)

## Fonctionalités 
* Extrement simple à utiliser.
* Design non-intrusif.
* S'intègre facilement avec d'autre paquet Go.
* Excellent reconnaissance de path et route.
* Design modulaire - Simplicité pour ajouter une fonctionnalité.
* Beaucoup de gestionnaires/middlewares à utiliser.
* Great 'out of the box' feature set.
* **Compatible complétement avec [http.HandlerFunc](http://godoc.org/net/http#HandlerFunc) interface.**

## Plus de middleware
Pour plus de middleware et de fonctionnalité, récupèrer le repo dans l'organisation  [martini-contrib](https://github.com/martini-contrib).

## Table des matières
* [Classic Martini](#classic-martini)
  * [Gestionnaires](#handlers)
  * [Routing](#routing)
  * [Services](#services)
  * [Serving Static Files](#serving-static-files)
* [Middleware Handlers](#middleware-handlers)
  * [Next()](#next)
* [Envirronement de martini](#martini-env)
* [FAQ](#faq)

## Classic Martini
To get up and running quickly, [martini.Classic()](http://godoc.org/github.com/go-martini/martini#Classic) provides some reasonable defaults that work well for most web applications:
~~~ go
  m := martini.Classic()
  // ... middleware and routing goes here
  m.Run()
~~~
