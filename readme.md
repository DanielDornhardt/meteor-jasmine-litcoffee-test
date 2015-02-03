Meteor-Jasmine-Litcoffee - Unit Testing - Example Project
===

This is a minimal example project to highlight the following error which occurs on my machine when trying to write a
server side unit test with jasmine and a .litcoffee - file is included in the project.

Some component of the testing stack seems to try to interpret the .litcoffee's (See [literate coffeescript](http://coffeescript.org/#literate)) text component (all the text which isn't indented)
as literal code, at least that's mt interpretation.

The following is written on my console after launching meteor with this code:


    [[[[[ ~/projects/DDD/meteor/learn/meteor-jasmine-litcoffee ]]]]]

    => Started proxy.
    => Started MongoDB.
    => Started your app.

    => App running at: http://localhost:3000/
    I20150203-14:24:04.161(1)? Hello Meteor, Jasmine and .litcoffee
    W20150203-14:24:04.429(1)? (STDERR) connections property is deprecated. Use getConnections() method
    I20150203-14:24:04.559(1)? unexpected ==
    I20150203-14:24:04.560(1)?   at /Users/spaceman/projects/DDD/meteor/learn/meteor-jasmine-litcoffee/meteor-jasmine-litcoffee.litcoffee:1
    W20150203-14:24:04.561(1)? (STDERR) [sanjo:jasmine]: { [SyntaxError: unexpected ==]
    W20150203-14:24:04.561(1)? (STDERR)   location: { first_line: 1, first_column: 0, last_line: 1, last_column: 1 },
    W20150203-14:24:04.561(1)? (STDERR)   toString: [Function],
    W20150203-14:24:04.561(1)? (STDERR)   code: 'Litcoffee Example\n===\n\n    Meteor.startup ->\n      console.log "Hello Meteor, Jasmine and .litcoffee"',
    W20150203-14:24:04.562(1)? (STDERR)   filename: undefined }