A simple example that demonstrates the different behaviour of webpack when running on a case sensitive versus insensitive filesystem.

This example is meant to be run on MacOs

## Scenario

The build run through webpack starts from index.js and imports the Foobar.js file.

The actual filename is `Foobar` but the import states `FooBar`

## Case insensitive filesystem

Run `npx webpack` on MacOs and the build will be successful

## Case sensitive filesystem

Run through docker with `docker image build -t itfails .` and the build will fail with error `Can't resolve './FooBar' in '/usr/src/app/src'`
