---
title: Interchange
layout: project
---

![interchange-screenshots.png](assets/interchange-screenshots.png "Screenshots of Interchange.")

**An iOS app for college transit, currently available for Chapman University.**
View routes, shuttle locations, and estimated arrival times in a sleek,
easy-to-use interface. I built this app using SwiftUI, Node.js and Apollo
GraphQL, with Redis as a primary storage mechanism.

[Download on the App Store](https://apps.apple.com/us/app/interchange-college-commute/id6739968742){: .primary-action }
[Join the TestFlight](https://testflight.apple.com/join/HbuHfUgW){: .secondary-action }
[Website](https://interchange.bchen.dev/){: .secondary-action }
{: .horizontal-wrapper }

## Design and implementation

The server is built using Node.js. I designed a basic GraphQL schema and
used [Apollo's GraphQL implementation](https://www.apollographql.com/docs/apollo-server/getting-started) to bring it to life.

In GraphQL, data is represented using a schema, which is then fulfilled with
resolvers defined in code. Each resolver function gets some information like the
parent object, arguments, and a server-defined shared context. Seeing the dependency injection that you could do with this context, I decided on an object-oriented approach consisting of **loaders**, **repositories**, and **systems**. Loaders load data from an external source, repositories store data, and systems are composed from a set of both loaders and repositories.

I then applied an event-driven pattern to implement the iOS notification sender, listening to updates on the shuttle repository. I would eventually reuse this pattern to implement an ETA prediction system that could run independently of an external data source.

