# MyCineList

I developed a fully-featured movie listing iOS application that integrates with The Movie Database (TMDB) API to provide users with an engaging and responsive movie browsing experience. The app features a dynamic home screen, bookmarking functionality, offline data support, search, and sharing capabilities.

Features & Implementation:

Home Screen with Trending & Now Playing Movies
The app showcases two distinct sections on the home screen: Trending Movies and Now Playing.

Pagination is implemented in the Now Playing section to support infinite scrolling, offering a seamless content consumption experience.

Movie Detail Screen
A dedicated detail screen displays comprehensive information about each movie. Users can navigate to this screen from the Home, Search, or Watchlist tabs by tapping on any movie item.

Bookmarking & Watchlist Functionality
Each movie cell includes a bookmark toggle, allowing users to add or remove movies from their personalized Watchlist. Bookmarked movies are easily accessible under the Watchlist tab.

Core Data Integration for Offline Support
All API responses are stored using Core Data, ensuring data persistence. In offline mode or during server downtime, the app continues to function by loading movies from local storage.

Search Functionality with Local Data
A search bar allows users to quickly find movies within the locally cached Trending and Now Playing lists. This ensures fast, offline-capable searching without making additional API calls.

Optimized Search with Debouncing
To enhance performance and reduce redundant queries, a debouncing mechanism using `DispatchWorkItem` is implemented. This ensures that searches are triggered efficiently after users pause typing.

Share Functionality
Users can share their favorite movies via a native share sheet. Tapping the Share button on the Movie Detail screen presents options to share the movie poster URL with others.

Image Caching for Enhanced Performance
A lightweight image caching system minimizes redundant network calls and significantly improves scrolling smoothness and overall performance.

