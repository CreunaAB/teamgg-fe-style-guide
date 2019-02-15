# Dependencies

Dependency refers to all the libraries, frameworks, and other tools that a project relies on.

* Install project dependencies via [npm](https://www.npmjs.com) whenever possible. 
* Always think twice before including a third-party library. Is this something we can build ourselves?
* Save packages that will be bundled as assets to _devDependencies_, general _dependencies_ are reserved for packages utilized by the Node process.
```
// Example package.json

{
    [...]
    "dependencies": {
        "express": "X.X.X"
    },
    "devDependencies": {
        "react": "X.X.X"
    }
}
```