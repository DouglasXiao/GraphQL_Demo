GRAPHQL DEMO SITE
=====================

A wrapper around [The Star Wars API](http://swapi.co) built using GraphQL converting it into [this schema](schema.graphql).

## Getting Started

Install dependencies with

```sh
npm install
```

## Local Server

A local express server is in `./server`. It can be run with:

```sh
npm run build
npm run start
```

A GraphiQL instance will be opened at http://localhost:xxxx/ (the actual port number will be printed to the console) to explore the API.

## Explore the Web Site
Send out the queries, there are several schemas to use with (Paste one of the following schemas into the left column and click on the PLAY button on left up corner): 

### film schema
{
  allFilms
  {
    films
    {
      title
      episodeID
      openingCrawl
      director
      producers
      releaseDate
    }
  }
}

### person schema
{
  allPeople
  {
    people
    {
      name
      birthYear
      eyeColor
      gender
      hairColor
      height
      mass
      skinColor
      homeworld
      {
        name
        diameter
        rotationPeriod
        orbitalPeriod
        gravity
        population
        climates
      }
    }
  }
}

### planet schema
{
  allPlanets {
    planets {
      name
      diameter
      rotationPeriod
      orbitalPeriod
      gravity
      population
      climates
      terrains
      surfaceWater
    }
  }
}

### species schema
{
  allSpecies {
    species {
      name
      classification
      designation
      averageHeight
      averageLifespan
      eyeColors
      hairColors
      skinColors
      language
      homeworld {
        name
        diameter
        rotationPeriod
        population
      }
    }
  }
}

### starship schema
{
  allStarships {
    starships {
      name
      model
      starshipClass
      manufacturers
      costInCredits
      length
      crew
      passengers
      maxAtmospheringSpeed
      hyperdriveRating
      MGLT
      cargoCapacity
      consumables
    }
  }
}

### vehicle schema
{
  allVehicles {
    vehicles {
      name
      model
      vehicleClass
      manufacturers
      costInCredits
      length
      crew
      passengers
      maxAtmospheringSpeed
      cargoCapacity
      consumables
    }
  }
}

### How to use the buttons (From left to right)
Play button: to fulfill the queries in left column and show responses in the right column
Prettify button: to prettify the JSON format.
History button: click on the History button so that you can see the history queries you have been made.

References:

* [graphql-js](https://github.com/graphql/graphql-js) - a JavaScript GraphQL runtime.
* [DataLoader](https://github.com/facebook/dataloader) - for coalescing and caching fetches.
* [express-graphql](https://github.com/graphql/express-graphql) - to provide HTTP access to GraphQL.
* [GraphiQL](https://github.com/graphql/graphiql) - for easy exploration of this GraphQL server.