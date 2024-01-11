<h1 align="center">
    sexpression_test</br>
    <span style="font-size: 1.25rem">
        powered by 
        ✨<a href="https://github.com/dmmulroy/create-melange-app">create-melange-app✨</a>
    </span>
</h1>

### Table of Contents

- [Getting Started](#getting-started)
- [Your project layout](#your-project-layout)
- [Installing OCaml packages](#installing-OCaml-packages)
- [Getting Help](#getting-help)

## Getting Started

Welcome to your `Melange` & `OCaml` app!

### Running your application

To run your application and start a dev server with hot module reloading, simply
run:

```sh
npm run dev
```

### Building your application

Building your application is as simple as running:

```sh
npm run build
```

This will handle running `Melange`'s build process and bundling your application
with `Vite`. Your bundled application and output will be located in `./dist`
after the build process completes.

## Your project layout

The following is a high level view of your project and application.
Many of these files will contain additional comments, explanations, examples,
and help for learning and getting started with `OCaml` and `Melange.`

```
sexpression_test
├── src
│   │   // This is a React Component and the entry point to your application
│   ├── App.re
│   │
│   │   // This is an example of how you can create additional React Components
│   ├── Configuration.re
│   │
│   │   // This directory is home to your bindings. Bindings are code you'll
│   │   // write to "bind" to and communicate with external JavaScript code.
│   ├── bindings
│   │   │
│   │   │   // This file controls exporting bindings that you write and makes
│   │   │   // them available to the rest of your project/code
│   │   ├── bindings.re
│   │   │
│   │   │   // This is an example of writing bindings to JavaScript DOM APIs
│   │   ├── browser.re
│   │   │
│   │   │   // This dune file configures your bindings library. In OCaml,
│   │   │   // each library has its own dune file. Generally, each library is
│   │   │   // contained in its own directory and is the standard way of
│   │   │   // organizing your code.
│   │   └── dune
│   │
│   │   // This directory is an example of a OCaml library. It contains
│   │   // code and modules used to interact with your projects configuration.
│   ├── create_melange_app
│   │   │
│   │   │   // This file controls exporting the modules within the
│   │   │   // `create_melange_app` library, making them available to the rest
│   │   │   // of your project/code.
│   │   ├── create_melange_app.re
│   │   │
│   │   │   // These are individual OCaml modules that compose the
│   │   │   // `create_melange_app` library.
│   │   ├── node_package_manager.re
│   │   ├── bundler.re
│   │   ├── configuration.re
│   │   │
│   │   │   // This `dune` file configures the `create_melange_app` library.
│   │   └── dune
│   │
│   │   // This `dune` file configures your root/application library. It wraps
│   │   // and composes all of the libraries that are used in your application.
│   │   // When you add new libraries to your project, you will need to add
│   │   // them to the `libraries` stanza in this file.
│   └── dune
│
│   // This directory is generated by 'Dune', OCaml's build tool.
│   // It contains compiled files and other artifacts from the build process.
│   // Note: This is _not_ where your application bundle/output/dist will be.
├── _build/
│
│   // This directory is created by `Opam`, OCaml's package manager. It
│   // contains your "local switch" and packages for your OCaml
│   // environment, specific to this project. You can think of the `_opam`
│   // folder and switches as OCaml's `node_modules`.
├── _opam/
│
│   // This is where your applications bundle or output will be located after
│   // running `npm run build`.
├── dist/
│
│   // This `dune` file configures `Melange`'s build process and settings. In
│   // addition, it also configures `Vite` to be ran by and integrated with
│   // `Dune`.
├── dune
│
│   // This file contains the overall configuration for your project, such as
│   // the name, version, metadata, and dependencies other settings understood
│   // by `dune`. You can think of this file as OCaml's `package.json`.
├── dune-project
│
│   // This file is generated by `Dune` and should not be manually edited. It
│   // Similar to your `dune-project` file, it contains dependencies and
│   // configuration settings for building your project. It is also similar to
│   // `package.json`. In the near future, `Dune` and `Opam` will be more
│   // tightly integrated as one tool.
├── first_try.opam
│
├── index.html
├── package-lock.json
├── package.json
├── vite.config.js
├── README
└── node_modules/
```

## Installing OCaml packages

Installing OCaml packages is easy, but we have to use a separate
CLI ([for the time being](https://github.com/dmmulroy/create-melange-app/issues/61)). To intsall dependencies, we are
going to use `opam`, which is OCaml's package manager. You can
search for dependencies and packages on
[OCaml.org](https://ocaml.org/packages/search?q=).

There are [some requirements](https://discuss.ocaml.org/t/whats-possible-with-melange/13806/3?u=dmmulroy) to use a package with `Melange` you should read
about. That being said, once you find a pakcage you want to install you can
do the following steps:

1. Add the library to your `dune-project`'s `depends` section
2. Run the following commands

```sh
eval $(opam env) # This activates your local switch in your shell
dune build sexpression_test.opam # This will regenerate your `opam` file
opam update # This will ensure `opam` can see the most recent versions of packages
opam install . --deps-only --yes # This will install your new packages
```

## Getting Help

- [OCaml's official site](https://ocaml.org)
- [ReasonML's official site](https://reasonml.github.io/)
- [Melange Docs](https://melange.re)
- [OCaml Discuss Forums](https://discuss.ocaml.org/)
- [The Caravan Discord Server](https://discord.gg/fNvVdsUWHE) - This is where
  the maintainers of `create-melange-app` hang out!
- [OCaml Discord Server](https://discord.gg/Qpzjmc4t)
- [ReasonML Discord Server](https://discord.gg/jPEH58TU)