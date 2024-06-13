# Redux

## Terminology
- `Redux` - a pattern and library for managing and updating application state using events called actions
  - helps manage the global state - the state needed across many application parts
- `actions` - events used by Redux to manage and update aplication state
- `store` - the center of every Redux application; a container that holds an application's global state
  - a javascript object with:
    - must never directly modify or change hte state that is kept inside the Redux store
    - only way to cause an update to the state is to create a plain action object that describes "something that happened in the application", and then dispatch the action to the store to tell it what happened
    - when an action is dispatched, the store runs the root reducer function, and lets it calculate the new state based on the old state and the action
    - store notifies subscribers that the state has been updated so the UI can be updated with the new data

## Useful When
1. app has a medium or large-sized codebase, and might be worked on by many people
2. app state is updated frequently over time
3. large amounts of application state that are needed in many places in the app
4. logic to update that state may be complex

## Installation
```
npm install @reduxjs/toolkit
```
- Redux Toolkit includes the Redux core, as well as other key packages we feel are essential for building Redux applications

## Next.js using the `with-redux` template
```
npx create-next-app --example with-redux my-app
```

## npm
View locally installed packages withotu every package's dependencies:
```
npm list -g --depth=0
```