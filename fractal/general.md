# General

* Each component should at minimum contain a `.hbs` and a `config.js` file.
* Set the status of the component in the config file. Component status should be set to either *wip* (work in progress) or *ready*.
* Use the context property in the config file to allow for dynamically changing component content and state.
```
// Sample config file
module.exports = {
    name: 'Input',

    status: 'wip',

    context: {
        label: 'Name',
        type: 'text',
        required: true
    }
}
```
* Use the variants property...