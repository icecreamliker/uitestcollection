# IndigoUnited/automaton

> github：https://github.com/IndigoUnited/automaton  

> Star: 220  
> Fork: 11  
> Watch: 20     
> Up to 2016.08.17 

## WHY?
You often find yourself needing to do some repetitive operation, and this is usually the time to quickly bake some ad-hoc script. Still, from project to project you find yourself needing to reuse some task you had already previously created.

Automaton eases this process, allowing you to quickly set up an autofile, which describes what you want to do, by means of an ordered list of tasks that need to run for the task as a whole to be complete.

A little detail that makes Automaton a powerful tool, is that every autofile you create can itself be used by another autofile, turning the first one into a single task (imagine boxes within boxes). If you are curious, you can take a look at the source code, and check for yourself that even the tasks that Automaton provides built-in are simple autofiles.  

### Simple Task

```javascript
module.exports = function (task) {
    task
    .id('my-task')
    .name('My task')
    .do('mkdir', {
        description: 'Create the project root folder',
        options: {
            dirs: ['some_dir']
        }
    })
    .do('cp', {
        description: 'Copy some file',
        options: {
            files: {
                'some_file': 'some_dir/dest_file'
            }
        }
    });
};
```

### Run with nodejs

```javascript
var automaton = require('automaton').create(/*options go here*/);

// Since autofiles are node modules themselves,
// you can just require them
// Note that you could have instead declared
// the module inline, in JSON.
var myTask = require('my_autofile');

// Note that we're running a task that you have loaded using node's
// require, and passing it as the first argument of the run() function.
// Instead, you can load the task using loadTask(), and then simply
// pass its id (a string), as the first argument of run. You can find an
// example of this below, in the Logging section.
automaton.run(myTask, { 'some_option': 'that is handy' }, function (err) {
    if (err) {
        console.log('Something went wrong: ' + err.message);
    } else {
        console.log('All done!');
    }
});
```

### Grunt Task

```javascript
module.exports = function (task) {
    task
    .id('bogus')
    .do('mincss', {
        grunt: true,
        options: {
            files: {
                'path/to/output.css': 'path/to/input.css'
            }
        }
    });
};
```