---
title: User Public Keys API v3 | developer.github.com
---

# User Public Keys API
Management of public keys via the API requires that you are
authenticated.

## List public keys

    GET /user/keys

### Response

<%= headers 200 %>
<%= json(:public_key) { |h| [h] } %>

## Get a public key

    GET /user/keys/:id

### Response

<%= headers 200 %>
<%= json :public_key %>

## Create a public key

    POST /user/keys

### Input

<%= json :title => "octocat@octomac", :key => "a public ssh key" %>

### Response

<%= headers 201 %>
<%= json :public_key %>

## Update a public key

    PATCH /user/keys/:id

### Input

<%= json :title => "octocat@octomac", :key => "a public ssh key" %>

### Response

<%= headers 200 %>
<%= json :public_key %>

## Delete a public key

    DELETE /user/keys/:id

### Response

<%= headers 200 %>
<%= json({}) %>
