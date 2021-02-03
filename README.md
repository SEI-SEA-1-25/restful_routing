# RESTful Resources & Routing

## Learning goals

- Start thinking about APIs in terms of the _resources_ they offer
- Get familiar with the 5 main RESTful routes, their HTTP verbs, and their nicknames.

## What is REST?

REST stands for \_Re_presentational \_S_tate \_T_ransfer. This acronym is the least important thing to take away from this exercise, so don't sweat it and save your brain cells for the important stuff.

It is important to remember: REST is a set of conventions that make it easier for developers to anticipate the structure of an API, which makes the task of reading the documentation much easier.

## What are resources?

A resource is any entity that an API can offer you. For example:

- [`https://openlibrary.org/developers/api`](https://openlibrary.org/developers/api) resources including books, covers, lists, subjects, etc.
- [`https://pokeapi.co/docs/v2`](https://pokeapi.co/docs/v2) offers resources that include pokemon, moves, items, etc.
  The documentation of an API should contain a thorough list of what resources it offers.

Note that when we talk about resources, we are talking about categories and not specific instances. For example, in the openlibrary API, books is a resource, but The Hobbit is an _instance_, not a resource. In the pokeapi, items is a resouce, but Super Potion is an instance.

## The Big 5 RESTful routes

For almost any resource, there are 5 main actions that we'll want to take on that resource, tabulated below. The columns are explained in more depth in later sections.

| Action                                                | Nickname | Route           | HTTP Verb |
| ----------------------------------------------------- | -------- | --------------- | --------- |
| See all available instances for the resource          | Index    | /{resources}    | GET       |
| See details about 1 specific instance of the resource | Show     | /{resource}/:id | GET       |
| Create a new instance of the resource                 | Create   | /{resources}    | POST      |
| Update an existing instance of the resource           | Update   | /{resource}/:id | PUT       |
| Delete an existing instance of the resource           | Delete   | /{resource}/:id | DELETE    |

## Nicknames

These make it easier to discuss APIs with another developer:

> Developer 1: Hey I heard you're building a social media API. What resources are you putting in it?

> Developer 2: Thanks for asking. It'll have users, posts, photos, and comments.

> D1: Oh wow. What actions are you going to allow for each resource?

> D2: For users, all 5. But for posts and comments, everything except update, because I don't want people changing the contents of their writing. For photos, just create and index because I'm lazy.

The goal of having these nicknames is that developers can share a lot of info quickly because they're working with similar assumptions.

## Routes

The strings in the routes column are making 3 assumptions:

1. {resource} is getting replaced with the name of an actual resource. BUT, pay attention to the pluralization! It is a non-optional part of the route.
1. The `:id` is a placeholder for the id of the instance you're taking action on. The leading `:` indicates that this segment of the route is a placeholder. In real life, ids are either numbers or strings.
1. The route string is getting concatenated onto the end of the hostname for this API to form the complete URL. You can't go into your browser and type in `/pokemon/ditto`, you have to append it like so: `https://pokeapi/api/v2/pokemon/ditto`.

## HTTP Verbs

Whenever you make an HTTP request, you need to supply at least 2 pieces of information: the URL that you are making the request to, and the _HTTP verb_ that you are using. You should get familiar with the verbs GET, POST, PUT, and DELETE. The verb is an essential part of the request, and changing the verb changes the request entirely. `GET /users/5` is very different from `DELETE /users/5`!

Whenever you type an address into your browser's URL bar and hit enter, you're making a GET request to that URL.
