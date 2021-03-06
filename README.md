**angular-github-api-factory** is an angularjs module with a github api factory.

[![npm version](https://badge.fury.io/js/angular-github-api-factory.svg)](https://badge.fury.io/js/angular-github-api-factory)
[![Bower version](https://badge.fury.io/bo/angular-github-api-factory.svg)](https://badge.fury.io/bo/angular-github-api-factory)

Author: Jonathan Hornung ([JohnnyTheTank](https://github.com/JohnnyTheTank))

## Usage

1. Install via either [bower](http://bower.io/), [npm](https://www.npmjs.com/) or downloaded files:
    1. `bower install --save angular-github-api-factory`
    2. `npm install --save angular-github-api-factory`
    3. download [angular-github-api-factory.zip](https://github.com/JohnnyTheTank/angular-github-api-factory/zipball/master)

2. Include dependencies in your HTML.
    1. When using bower:
    ```html
    <script src="bower_components/angular-github-api-factory/dist/angular-github-api-factory.min.js"></script>
    ```
    2. When using npm:
    ```html
    <script src="node_modules/angular-github-api-factory/dist/angular-github-api-factory.min.js"></script>
    ```
    3. when using downloaded files
    ```html
    <script src="angular-github-api-factory.min.js"></script>
    ```
3. Add **`jtt_github`** to your application's module dependencies.
4. Use the factory `githubFactory`

### factory methods

#### getUser
```js
githubFactory.getUser({
    user:"<USERNAME_NAME>",
    access_token:"<ACCESS_TOKEN>" // (optional)
}).then(function(_data){
    //on success
}).catch(function (_data) {
    //on error
});
```

#### getUsers
```js
// https://developer.github.com/v3/search/#search-users
githubFactory.getUsers({
    q:"<SEARCH_STRING>",  // (optional)
    sort:"<SORT_STRING>", // (optional) 'followers', 'repositories', 'joined'
    order:"<SORT_ORDER>", // (optional) 'desc', 'asc'
    per_page:"<ITEMS_PER_PAGE>", // (optional) valid values: 1-100 | default: 30
}).then(function(_data){
    //on success
}).catch(function (_data) {
    //on error
});
```

#### getRepo
```js
githubFactory.getRepoByUserAndName({
    user:"<USER_NAME>",
    repo:"<REPO_NAME>",
    access_token:"<ACCESS_TOKEN>" // (optional)
}).then(function(_data){
    //on success
}).catch(function (_data) {
    //on error
});
```

#### getRepos
```js
// https://developer.github.com/v3/search/#search-repositories
githubFactory.getReposByName({
    q:"<SEARCH_STRING>",
    sort:"<SORT_STRING>", // (optional) 'stars', 'forks', or 'updated'
    order:"<SORT_ORDER>", // (optional) 'desc', 'asc'
    per_page:"<ITEMS_PER_PAGE>", // (optional) valid values: 1-100 | default: 30
    access_token:"<ACCESS_TOKEN>" // (optional)
}).then(function(_data){
    //on success
}).catch(function (_data) {
    //on error
});
```

```js
githubFactory.getReposByUser({
    user:"<USER_NAME>",
    q:"<SEARCH_STRING>", // (optional)
    sort:"<SORT_STRING>", // (optional) 'stars', 'forks', or 'updated'
    order:"<SORT_ORDER>", // (optional) 'desc', 'asc'
    per_page:"<ITEMS_PER_PAGE>", // (optional) valid values: 1-100 | default: 30
    access_token:"<ACCESS_TOKEN>" // (optional)
}).then(function(_data){
    //on success
}).catch(function (_data) {
    //on error
});
```

#### getEvents
```js
githubFactory.getEventsFromRepoByUserAndName({
    user:"<USER_NAME>",
    repo:"<REPO_NAME>",
    q:"<SEARCH_STRING>",  // (optional)
    sort:"<SORT_STRING>", // (optional)
    order:"<SORT_ORDER>", // (optional) 'desc', 'asc'
    per_page:"<ITEMS_PER_PAGE>", // (optional) valid values: 1-100 | default: 30
    access_token:"<ACCESS_TOKEN>" // (optional)
}).then(function(_data){
    //on success
}).catch(function (_data) {
    //on error
});
```

```js
githubFactory.getEventsByUser({
    user:"<USER_NAME>",
    q:"<SEARCH_STRING>", // (optional)
    sort:"<SORT_STRING>", // (optional)
    order:"<SORT_ORDER>", // (optional) 'desc', 'asc'
    per_page:"<ITEMS_PER_PAGE>", // (optional) valid values: 1-100 | default: 30
    access_token:"<ACCESS_TOKEN>" // (optional)
}).then(function(_data){
    //on success
}).catch(function (_data) {
    //on error
});
```


## Github JSON API

* docs: https://developer.github.com/v3/

## More angular-api-factories
[bandsintown](https://github.com/JohnnyTheTank/angular-bandsintown-api-factory) - [dailymotion](https://github.com/JohnnyTheTank/angular-dailymotion-api-factory) - [facebook](https://github.com/JohnnyTheTank/angular-facebook-api-factory) - [footballdata](https://github.com/JohnnyTheTank/angular-footballdata-api-factory) - [flickr](https://github.com/JohnnyTheTank/angular-flickr-api-factory) - **github** - [openweathermap](https://github.com/JohnnyTheTank/angular-openweathermap-api-factory) - [tumblr](https://github.com/JohnnyTheTank/angular-tumblr-api-factory) - [vimeo](https://github.com/JohnnyTheTank/angular-vimeo-api-factory) - [wikipedia](https://github.com/JohnnyTheTank/angular-wikipedia-api-factory) - [youtube](https://github.com/JohnnyTheTank/angular-youtube-api-factory)

## License

MIT