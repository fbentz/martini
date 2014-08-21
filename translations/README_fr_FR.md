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


