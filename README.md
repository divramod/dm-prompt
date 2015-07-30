## Description
- A module for simplyfying the usage of nodejs prompts.
- Currently based on [inquirer](https://www.npmjs.com/package/inquirer)
- make it possible to yield a inquirer Prompt
- has to be used within [co](https://www.npmjs.com/package/co)
- [inquirer examples](https://github.com/SBoudrias/Inquirer.js/tree/master/examples)

## Installation

    npm install dm-prompt --save

## Usage

    var dmPrompt = require("dm-prompt").Inquirer;
    var co = require("co");

    var job = {};

    job.start = co.wrap(function*() {
        // for other options see inquirer examples
        var directoryAnswer =
            yield dmPrompt({
                type: "input",
                name: "directory",
                message: "Please state the Directory to where node_modules should link to:"
            });
        var directory = directoryAnswer.directory;
        console.log(directory);
    });

    module.exports = job;

## TODO
- wrap new Seperator()
