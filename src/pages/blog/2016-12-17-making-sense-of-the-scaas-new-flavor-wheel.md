---
templateKey: blog-post
title: Business applications reference architecture for 2017 and beyond?
date: 2016-12-30T15:04:00.000Z
description: >-
  In this article I present a reference architecture to develop business
  applications based on the rich clients web architecture that I described two
  years ago in the following article: The evolution of business applications
  architecture.
tags:
  - ''
---
The 6 criteria I used in selecting this reference architecture are the following:

1. Provides good performance on all clients
2. Simplifies development and maintenance
3. Enables reusable UI components
4. Is compatible with most infrastructures (for backend processing and storage)
5. Supports the most populars clients: All modern web browsers, desktop (Mac, Windows and Linux) and mobile (iOS and Android)
6. Is supported by a major industry player

This reference architecture is composed of 3 main elements:

1. React: This UI library developed by Facebook has been gaining real traction in 2016 in part because of it good performance and good component model.
2. GraphQL: This is a specification developed by Facebook that enables the clients to query the servers in an efficient and maintainable way and that effectively replace REST web services for most use cases.
3. Relay: This is the bridge developed by Facebook between React and GraphQL that provides an integrated end to end solution to develop rich clients web applications.

This reference architecture respond to the 6 criteria I defined at the start of this article:

Provides good performance on all clients

By replacing the REST web services with GraphQL you are able to reduce the amount of data sent over the network because GraphQL only return the precise data you requested. You are also able to reduce the number of calls to the server because GraphQL can return all the data you need in just one call to the server. Also by using the concept of a virtual DOM, React improve performance by reducing the numbers of modifications made to the DOM. Finally, by using native components on mobile devices, React Native improves the performance of mobile applications compared to hybride mobile applications, but still able to you to reuse code between your desktop, mobile and web applications.

Simplifies development and maintenance

By providing an integrated end to end solution between the UI components and the server this architecture reduce boilerplate code. This architecture also facilitates development and maintenance by replacing multiples REST endpoints that would need to be modified when the applications evolve with one GraphQL endpoint that can adapt to many applications evolutions without breaking compatibility with previous version of the applications and often without even needing any modification if it was well designed.

Enables reusables UI components

Providing reusable UI components is also key to simplifying application development and maintenance. By providing a clean component model where all the related part of a component are located together, React facilitate the development of reusables components. In addition Relay and GraphQL add the data requirements to the UI component, making the reusable components even more complete and reducing further boilerplate code.

Is compatible with most infrastructures (for backend processing and storage)

In many contexts you will not have complete liberty on the choice of infrastructures your applications will run and store their data. You may have existing infrastructures that would be very costly to replace. You may have talents with expertise with some infrastructures that would take time to train on new infrastructures. Or you just may have some specific requirement that need some type of infrastructures. The proposed architecture will work with most existing infrastructures. It is not dependant on any type of data storage and implementation of GraphQL already exists in many backend languages making it easy to deploy on your preferred infrastructures or even to change your infrastructures over time.

Supports the most populars clients: All modern web browsers, desktop (Mac, Windows and Linux) and mobile (iOS and Android)

In today environment, business applications need to be accessible on many different clients but you also want to reduce the cost of developing and maintaining different applications for different clients. The architecture proposed in this article will support all majors browsers, but you often also want to be able to create desktop versions of your applications for all major OS (Mac, Windows and Linux) and mobile versions of your applications for iOS and Android. By extending the proposed architecture using React Native for the mobile and using Electron for the desktop you will be able to create those applications by reusing a significant portion of the code you developed for the web version.

Is supported by a major industry player

The rich clients web applications market is very big and the architecture that will dominate this market will have significant impact on the software industry. Also developing and maintaining this architecture is costly and the companies that would be using this architecture to develop their applications will have to make significant investments to convert to any given architecture. For those reasons, I don’t believe it is possible for a small player to dominate this market in the long terme. The architecture that will dominate this market will need to be fully supported by at least one major player. In this case this major player is Facebook for all 3 main components of the architecture (React, GraphQL and Relay). This will insure the perennity of this architecture and will reassure others companies to use this architecture.

Conclusion

In conclusion, even if the market for rich clients web applications is still fragmented and there is still place for a new player to emerge and shift the market, the architecture presented in this article as some uniques advantages. To my knowledge, it is the first time since the shift to a rich clients web architecture that we have an architecture that meet the 6 criteria I presented in this article. AngularJS tried to dominate this market and was supported by a major industry player (Google) but lacked in performance and was not offering an end to end solution. Meteor also tried to dominate this market by offering an end to end solution, but was dependent on very specific infrastructures (NodeJS and MongoDB) and didn’t have the full support of a major industry player like Google or Facebook. To my knowledge this architecture is the first to meet the 6 criteria defined in this article and, in my opinion, is the first that has a real chance of dominating the rich clients web applications market in the years to come.
