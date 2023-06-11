##### Backgrounds API Documentation

Welcome to the documentation for the Backgrounds API. The Backgrounds API is a free public API that provides a collection of fivem backgrounds. With this API, you can access a wide range of backgrounds to enhance the visual appeal of your projects. The API offers two main routes: `/random` and `/list`. Please read below for details on how to utilize these routes effectively.

##### Base URL

The base URL for accessing the Backgrounds API is `https://backgrounds.adrencad.com`.

##### Route: `/random` (GET)

This route allows you to retrieve a random background from the available collection.

##### Request

-   Method: GET
-   Endpoint: `/random`

##### Response Parameters

-   creditor (string): The author of the background.
-   credit (string): The link to the creditor's store.
-   src (string): The URL pointing to the background image.

#### Example Response

```
{
  background: {
    creditor: "Jayce H.",
    credit: "https://discord.gg/jaycesworkshop",
    src: "https://i.imgur.com/NHkIdFp.png"
  }
}
```

##### Route: `/list` (GET)

This route allows you to fetch all the available backgrounds from the API's collection.

##### Request

-   Method: GET
-   Endpoint: `/list`

#### Example Response

```
{
  backgrounds: [
    {
      creditor: "Jayce H.",
      credit: "https://discord.gg/jaycesworkshop",
      src: "https://i.imgur.com/pG7rvdy.png"
    },
    {
      creditor: "Jayce H.",
      credit: "https://discord.gg/jaycesworkshop",
      src: "https://i.imgur.com/LVemN2f.png"
    },
    {
      creditor: "Jayce H.",
      credit: "https://discord.gg/jaycesworkshop",
      src: "https://i.imgur.com/NHkIdFp.png"
      }
    ]
  }
```
