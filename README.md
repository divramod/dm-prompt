## Description
- A module for simplyfying the usage of nodejs prompts.
- Currently based on [inquirer](https://www.npmjs.com/package/inquirer)
- make it possible to yield a inquirer Prompt
- has to used within [co](https://www.npmjs.com/package/co)

## Installation

    npm install dm-prompt --save

## Usage

    var dmPrompt = require("dm-prompt");
    var co = require("co");

    var job = {};

    job.start = co.wrap(function*() {
        // for other options see https://github.com/SBoudrias/Inquirer.js/tree/master/examples
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


// =========== [ MODULE EXPORT ] ===========
module.exports = job;
    var name

## TODO
- wrap new Seperator()
