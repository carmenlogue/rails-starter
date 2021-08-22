# Rails starter

Este es un proyecto que contiene los elementos básicos para comenzar un proyecto profesional en Ruby on Rails.

Si quieres conocer los detalles visita [HolaRuby!](https://holaruby.com/starter_list)

[![Build Status](https://app.travis-ci.com/carmenlogue/rails-starter.svg?branch=main)](https://app.travis-ci.com/carmenlogue/rails-starter)
[![Maintainability](https://api.codeclimate.com/v1/badges/018bfc8519adf41a80a9/maintainability)](https://codeclimate.com/github/carmenlogue/rails-starter/maintainability)

## Entorno de desarrollo local

- [Docker](https://docs.docker.com/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Configuración

Clona el proyecto desde https://github.com/carmenlogue/rails-starter y después ejecuta:
    
    cd rails-starter
    docker-compose build

## Para empezar localmente

Para arrancar los servicios necesario para trabajar localmente ejecuta:

    docker-compose up

Y visita http://localhost:3000/

## Actualizar dependencias

Las gemas de ruby se instalan con docker build, para hacer cambios en las dependencias necesitas actualizar el `Gemfile`y ejecuta de nuevo:

    docker-compose build

## Ejecuta comandos

Como el proyecto se ejecuta en docker, para abrir una consola de ruby, correr migraciones o ejecutar tareas necesitas ejecutar lo siguiente:

    docker-compose run web bash
    rails c

## Mail

Cualquier email lanzado desde el entorno local de desarrollo se captura con Mailcatcher, y se pueden ver en http://localhost:1080/

## Flujo de trabajo

Desarrolla en ramas que salgan de la rama principal `main`, después genera una pull request.

Una vez la pull request tiene los checks verdes (rubocop y rspec) y está aprobada se puede mergear en `main`.
