sublime-grunt
=============

Originally forked from https://github.com/tvooo/sublime-grunt with a dirty hack added to allow you to specify a command to run.

You can now key bind to a command using the following. 

```
[
	{"keys": ["ctrl+b"], "command": "grunt", "args": {"command" : "default"}}
] 
```
This is moderately dirty because if you use muliple grunt files it will running the same command for each file. But for most users who only use one grunt file this is perfect.

A Grunt task runner for Sublime Text



![Screencast of sublime-grunt](screencast.gif)

## Installation

```
cd ~/.config/sublime-text-3/Packages
git clone git@github.com:glitcha/sublime-grunt.git Grunt
```

## Usage

Open the command palette using Ctrl+Shift+P (or Cmd+Shift+P on Mac, respectively)
and choose the "Grunt" command.

The plugin expects to find a Gruntfile (`Gruntfile.js` or `Gruntfile.coffee`) in an open folder.
It displays a sorted list of available Grunt tasks out of this Grunt file.
If it finds more than one Gruntfile, it first provides a list for selection.

As of version 0.2, there is also a command to kill running tasks, for example
`watch` tasks.

## Settings

The file `SublimeGrunt.sublime-settings` is used for configuration.

You may override your `PATH` environment variable as follows:

```
{
    "exec_args": {
        "path": "/bin:/usr/bin:/usr/local/bin"
    }
}
```
If your GruntFile is not in the base path of the project, then you can add the path(s) to check as follows:

```
{
    "gruntfile_paths": ["/path", "/another/path", "/one/final/path"]
}
```
Alternatively this could be set per-project in your .sublime-project settings object

## Releases

* 1.0 Jumping to 1.0 to support ST versioning with tags
* 0.3 Grunt tasks are cached
* 0.2 Rewrite; supports Grunt >= 0.4, tasks can be killed (for example the `watch` task)
* 0.1 Initial release

## Thanks

Thanks for some contributions go to

* [VirtueMe](https://github.com/VirtueMe)
* [antonellopasella](https://github.com/antonellopasella)
* [structAnkit](https://github.com/structAnkit)
* [lavrton](https://github.com/lavrton)
* [adamcbrewer](https://github.com/adamcbrewer)
* [thebjorn](https://github.com/thebjorn)
* [maliayas](https://github.com/maliayas)
