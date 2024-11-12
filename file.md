# yargs 
- Yargs გვეხმარება შევქმნათ ინტერაქტიული command line tools, არგუმენტების ანალიზით და მომხმარებლის ინტერფეისის გენერირებით.
## The builder 
- function is used to define the options and parameters for a specific command. It allows you to specify arguments, types, default values, descriptions, and whether they are required or optional. Essentially, it "builds" the structure of the command's options.
```js
yargs.command(
  'greet [name]',
  'Greet a user by name',
  (yargs) => {
    return yargs
      .positional('name', {
        describe: 'Name of the person to greet',
        type: 'string',
        default: 'World'
      })
      .option('enthusiasm', {
        alias: 'e',
        describe: 'Add enthusiasm to the greeting',
        type: 'boolean',
        default: false
      });
  },
  (argv) => { /* handler function */ }
)
```
## handler
- The handler function is where the logic of the command is implemented. This function is executed when the command is called, and it receives the parsed arguments as its argv parameter. You use argv to access the command options and implement the desired behavior.
---
# chalk
- chalk is a popular Node.js library for styling and coloring text in the terminal. It helps make command-line outputs more readable and visually appealing, which is especially useful for logging, error messages, and other feedback.
---
# express 
- What Is Express JS? Express is a node js web application framework that provides broad features for building web and mobile applications. It is used to build a single page, multipage, and hybrid web application.
- Express შეიქმნა API-ების და ვებ აპლიკაციების მარტივად გასაკეთებლად,ის დაზოგავს უამრავ კოდირების დროს თითქმის ნახევარით და მაინც ქმნის ვებ დამობილური აპლიკაციები ეფექტურია. Express-ის გამოყენების კიდევ ერთი მიზეზი არის ის, რომ ის იწერება Javascript-ში, რადგან javascript არის მარტივი ენა, მაშინაც კი, თუ არ გაქვთ წინა ნებისმიერი ენის ცოდნა. Express საშუალებას აძლევს ამდენ ახალ დეველოპერს შევიდეს ვებ განვითარების სფეროში. Node js-ისთვის ექსპრეს ჩარჩოს შექმნის მიზეზი არის:
- დროში ეფექტური
- სწრაფი
- ეკონომიური
- მარტივი სწავლა
- ასინქრონული
---
# In Node.js, modules 
- are individual files or packages of code that can be loaded into a Node application. They help structure and organize code, promote reusability, and make dependency management straightforward. Node.js has a built-in module system that allows you to use both built-in modules (provided by Node itself) and user-defined modules (code you write or install from external sources like npm).
- Types of Modules in Node.js Core Modules
- Node.js provides a set of core modules (like fs, http, path, os, etc.) that come bundled with Node.js, so you don’t need to install them.
- These core modules handle common functionalities like file manipulation, network requests, path operations, and more.
- const fs = require('fs'); // Importing the 'fs' (File System) core module
fs.readFile('file.txt', 'utf8', (err, data) => {
  if (err) throw err;
  console.log(data);
});
---
# npm install 
- The command npm install is used with Node Package Manager (npm) to install packages (or modules) for a Node.js project. It’s a versatile command that can handle several tasks related to package installation.
Common Uses of npm install
- Install a Specific Package
- When you specify a package name, npm install <package-name>, npm installs that package along with its dependencies.
- npm install express
- This will download the express package and its dependencies, placing them in a node_modules folder in your project.
- By default, npm installs packages in dependencies (in your package.json), which means they’re needed for your app to run.
- Install All Dependencies in package.json
- When run without any arguments, npm install will install all the dependencies listed in your package.json file.
- npm install
- This command is commonly used when you clone or download a project from a repository. Running npm install will install all the required dependencies for the project to run.
- Install Packages as a Development Dependency
- Adding the --save-dev or -D flag installs a package as a development dependency. These are packages you only need for development (e.g., testing or build tools) and not for production.
- npm install eslint --save-dev
- Install Specific Versions
- If you want a specific version of a package, you can specify it after the package name with @.
- npm install lodash@4.17.21
- Global Installation
- By adding the -g or --global flag, npm install installs a package globally, making it available across all projects on your system.
- npm install -g nodemon
## Summary of npm install
- installs and manages dependencies for a project.
- Downloads specific packages, either globally or locally.
- Enables installation of all dependencies listed in package.json, making it essential when setting up an existing project.
- This command is central to working with Node.js projects, ensuring they have the required modules and tools to function correctly.
