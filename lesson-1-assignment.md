### Assignment 1:

**1. Fetch Boba Fett, get the name:**
```graphql
{
  person(personID: 22) {
    name
  }
}
```
```json
{
  "data": {
    "person": {
      "name": "Boba Fett"
    }
  }
}
```

**2. Get Yoda's name, height, and eye color:**
```graphql
{
  person(personID: 20) {
    name
    height
    eyeColor
  }
}
```
```json
{
  "data": {
    "person": {
      "name": "Yoda",
      "height": 66,
      "eyeColor": "brown"
    }
  }
}
```

**3. Get Obi-Wan Kenobi, include the name and name of the homeworld:**
```graphql
{
  person(personID: 10) {
    name
    homeworld {
      name
    }
  }
}
```
```json
{
  "data": {
    "person": {
      "name": "Obi-Wan Kenobi",
      "homeworld": {
        "name": "Stewjon"
      }
    }
  }
}
```

**4. Get the total count of all species:**
```graphql
{
  allSpecies {
    totalCount
  }
}
```
```json
{
  "data": {
    "allSpecies": {
      "totalCount": 37
    }
  }
}
```

**5. Get the name of all vehicles:**
```graphql
{
  allVehicles {
    vehicles {
        name
    }
  }
}
```
```json
{
  "data": {
    "allVehicles": {
      "vehicles": [
        {
          "name": "Sand Crawler"
        },
        {
          "name": "T-16 skyhopper"
        },
        {
          "name": "X-34 landspeeder"
        },
        {
          "name": "TIE/LN starfighter"
        },
        {
          "name": "Snowspeeder"
        },
        {
          "name": "TIE bomber"
        },
        {
          "name": "AT-AT"
        },
        {
          "name": "AT-ST"
        },
        {
          "name": "Storm IV Twin-Pod cloud car"
        },
        {
          "name": "Sail barge"
        },
        {
          "name": "Bantha-II cargo skiff"
        },
        {
          "name": "TIE/IN interceptor"
        },
        {
          "name": "Imperial Speeder Bike"
        },
        {
          "name": "Vulture Droid"
        },
        {
          "name": "Multi-Troop Transport"
        },
        {
          "name": "Armored Assault Tank"
        },
        {
          "name": "Single Trooper Aerial Platform"
        },
        {
          "name": "C-9979 landing craft"
        },
        {
          "name": "Tribubble bongo"
        },
        {
          "name": "Sith speeder"
        },
        {
          "name": "Zephyr-G swoop bike"
        },
        {
          "name": "Koro-2 Exodrive airspeeder"
        },
        {
          "name": "XJ-6 airspeeder"
        },
        {
          "name": "LAAT/i"
        },
        {
          "name": "LAAT/c"
        },
        {
          "name": "AT-TE"
        },
        {
          "name": "SPHA"
        },
        {
          "name": "Flitknot speeder"
        },
        {
          "name": "Neimoidian shuttle"
        },
        {
          "name": "Geonosian starfighter"
        },
        {
          "name": "Tsmeu-6 personal wheel bike"
        },
        {
          "name": "Emergency Firespeeder"
        },
        {
          "name": "Droid tri-fighter"
        },
        {
          "name": "Oevvaor jet catamaran"
        },
        {
          "name": "Raddaugh Gnasp fluttercraft"
        },
        {
          "name": "Clone turbo tank"
        },
        {
          "name": "Corporate Alliance tank droid"
        },
        {
          "name": "Droid gunship"
        },
        {
          "name": "AT-RT"
        }
      ]
    }
  }
}
```

**6. List all of Luke's vehicles:**
```graphql
{
  person(personID: 1) {
    name
    vehicleConnection {
      vehicles {
        name
      }
    }
  }
}

```
```json
{
  "data": {
    "person": {
      "name": "Luke Skywalker",
      "vehicleConnection": {
        "vehicles": [
          {
            "name": "Snowspeeder"
          },
          {
            "name": "Imperial Speeder Bike"
          }
        ]
      }
    }
  }
}
```

**7. List the name of all of Vader's starships including the maxAtmospheringSpeed:**
```graphql
{
  person(personID: 4) {
    name
    starshipConnection {
      starships {
        name
        maxAtmospheringSpeed
      }
    }
  }
}

```
```json
{
  "data": {
    "person": {
      "name": "Darth Vader",
      "starshipConnection": {
        "starships": [
          {
            "name": "TIE Advanced x1",
            "maxAtmospheringSpeed": 1200
          }
        ]
      }
    }
  }
}
```

**8. Get both R2-D2 and C-3PO's names and eye colors. Use a single query to get both characters!:**
```graphql
{
  r2: person(personID: 3) {
    name
    eyeColor
  }
  c3po: person(personID: 2) {
    name
    eyeColor
  }
}
```
```json
{
  "data": {
    "r2": {
      "name": "R2-D2",
      "eyeColor": "red"
    },
    "c3po": {
      "name": "C-3PO",
      "eyeColor": "yellow"
    }
  }
}
```

**9. Get the name of Han and Chewbacca's homeworld. Use a single query to get the names of both worlds:**
```graphql
{
  han: person(personID: 14) {
    name
    homeworld {
      name
    }
  }
  chewbacca: person(personID: 13) {
    name
    homeworld {
      name
    }
  }
}
```
```json
{
  "data": {
    "han": {
      "name": "Han Solo",
      "homeworld": {
        "name": "Corellia"
      }
    },
    "chewbacca": {
      "name": "Chewbacca",
      "homeworld": {
        "name": "Kashyyyk"
      }
    }
  }
}
```

**10. List the title of all films with Leia, including the title and director:**
```graphql
{
  person(personID: 5) {
    name
    filmConnection {
      films {
        title
        director
      }
    }
  }
}
```
```json
{
  "data": {
    "person": {
      "name": "Leia Organa",
      "filmConnection": {
        "films": [
          {
            "title": "A New Hope",
            "director": "George Lucas"
          },
          {
            "title": "The Empire Strikes Back",
            "director": "Irvin Kershner"
          },
          {
            "title": "Return of the Jedi",
            "director": "Richard Marquand"
          },
          {
            "title": "Revenge of the Sith",
            "director": "George Lucas"
          }
        ]
      }
    }
  }
}