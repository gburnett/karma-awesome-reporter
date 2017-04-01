# karma-awesome-reporter

Test reporter, that prints detailed results to console (forked from the karma-spec-reporter).

## Usage

To use in your own Node.js project, just execute
```
npm install karma-awesome-reporter --save-dev
```
This will download the karma-awesome-reporter and add the dependency to `package.json`.

Then add ``'spec'`` to reporters in karma.conf.js, e.g.

```
reporters: ['awesome']
```


## Configuration

To limit the number of lines logged per test or suppress specific reporting, use the `specReporter` configuration in your
karma.conf.js file
``` js
//karma.conf.js
...
  config.set({
    ...
      reporters: ["awesome"],
      specReporter: {
        maxLogLines: 5,             // limit number of lines logged per test
        suppressErrorSummary: true, // do not print error summary
        suppressFailed: false,      // do not print information about failed tests
        suppressPassed: false,      // do not print information about passed tests
        suppressSkipped: true,      // do not print information about skipped tests
        showSpecTiming: false,      // print the time elapsed for each spec
        failFast: true              // test would finish with error when a first fail occurs.
      },
      plugins: ["karma-awesome-reporter"],
    ...
```

## Contributing

### Running tests

To run the tests for the index.js file, run: `npm test`

### Generating Coverage

To see the coverage report for the module, run: `npm run coverage`
