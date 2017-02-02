# iOS Challenge

Create an app in Swift that displays a list of Farmdrop producers and their details.

## Displaying a list of producers

### A) Use the following API endpoint (GET) to fetch a list of producers: 
- Use this enpoint: `https://fd-v5-api-release.herokuapp.com/2/producers`
- No authentication is required for this endpoint.
- Response will contain a JSON object.

1) Parse the JSON object to produce a smooth scrolling list of producers.

2) Each cell should at least contain:
- The producer's name (JSON key `name`).
- The producer's short description (`short_description`). Truncate it, if the length is more than ~3 / 4 lines long.

3) When tapping on a producer's cell, it should be possible to see a detailed view of that producer with the following information:
- The producer's name.
- The producer's image (`images`). Use the first one if there's more than one.
- The produceer's location (`location`) if available.
- The producer's long description (`description`) or the short description is no long description is avaliable.

Note: If you want, you can fetch an invididual producer's date by specifying their id: `https://fd-v5-api-release.herokuapp.com/2/producers/{id}`

### B) Add pagination to your list of producers created as part of task A. You can use the same endpoint, and pass the followwuing query parameters:
- `page`: The page number (first page is 1).
- `per_page_limit`: The size of the page.

NB: When there are no more pages, the `response` key will contain an empty array.

## Search locally for producers.

### 1) Persist the list of producers on the device.
- Use any technology or method you desire.
- Make sure that the list is kept up to date (or downloaded every time if you like) with the server data.

### 2) Add a searchbar to your list of producers created as part of task A.
- When the user types a string in that search bar, display only the producer's whose name contains the search string.
- Allow the user to cancel such or clear the search bar.


*****

## Requirements

### Submit as an xcode project
- You can fork this repository and submit a link to your fork.

### Extra 
- Use a reactive framework like ReactiveSwift (ReactiveCocoa) or RxSwift if you're familiar with it.
- Feel free to use third party frameworks for JSON parsing, networking, image caching and so on.
- Add unit tests.

*****

## <a name="evaluation_criteria"/>Evaluation criteria:

- Quality is better than quantity
- Maintain a consistent navigation structure, be it tabs or sliding menus
- Device orientation handling is not required, although we expect you to structure your code to be able to easily add support for this
- Architecture, how clean and structured the code is. 
- Our endpoints use the following http methods: POST, GET, PUT, PATCH, and DELETE, so choose a network framework that supports all of them.
- Compatibility with various devices and previous OS (iOS 9 and 10). Good use of additional libraries (if relevant).
- Use of built-in components, e.g.: UIStackView, UICollectionView, UISearchController, UITabBarController, UrlSession, URLRequest, CoreData, etc.
- Use of design patterns
- We make use of a lot of images, including using them for animation when navigating from screen to screen.
- Unit tests

*****

### **ATTENTION** ###

Do not directly PUSH to this repository!!!

