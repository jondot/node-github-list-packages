node-github-list-packages
=========================

A node modules that lists packages used by github projects

Give a repository URL this module would search for packages files of different platforms, analyze and list their dependencies.
So for example it would look for package.json and list the dependencies found in this file.

# Usage

```
npm install node-github-list-packages
```

```
lister = require('node-github-list-packages');
lister.getUsedPackages('https://github.com/rantav/node-github-list-packages', function(err, packageFiles) {
  console.log(_.union(_.pluck(packageFiles, 'packages')));
});
```

Or command line:
```
$ github-list-packages https://github.com/rantav/node-github-list-packages
```

# Supported Packagers
* NPM (package.json)
* Meteor (.meteor/package)
* Meteor Atmosphere (smart.json)
* Meteor NPM (packages.js)
* More to come...
