<p align="center">
  <h1 align="center">Laravel Inertia</h1>
  <p align="center">
    <a href="https://github.com/use-preset/use-preset/actions">
      <img alt="Build status" src="https://github.com/use-preset/laravel-inertia/workflows/tests/badge.svg">
    </a>
    &nbsp;
    <a href="https://github.com/use-preset/use-preset/releases">
      <img alt="npx use-preset laravel-inertia" src="https://img.shields.io/badge/use--preset-laravel--inertia-blue">
    </a>
    &nbsp;
    <a href="https://www.npmjs.com/package/use-preset">
      <img alt="use-preset version" src="https://img.shields.io/npm/v/use-preset?color=32c854&label=use-preset">
    </a>
  </p>
  <br />
  <p align="center">
    <b>Preset</b> is a project-modifying tool. <a href="https://usepreset.dev/">Read the documentation</a> for more information.
  </p>
  <br />
  <pre align="center">npx use-preset laravel-inertia</pre>
  &nbsp;
<p>

# About

This Laravel preset scaffolds an application using the **LIT** stack, jumpstarting your application's development. If you are not familiar with the name, it is an acronym that describes the main technologies involved in the stack:

| [Laravel](https://laravel.com/) | [Inertia](https://inertiajs.com) | [Tailwind CSS](https://tailwindcss.com/) |
| ------------------------------- | -------------------------------- | ---------------------------------------- |
| PHP framework                   | Modern monolith                  | Utility-first CSS framework              |

The **LIT** stack becomes the **VITL** stack if [Vue](https://vuejs.org) is added, or the **LITR** stack with [React](https://reactjs.org) instead.

# Installation

This preset is intended to be installed into a fresh Laravel application. Follow the [Laravel installation instructions](https://laravel.com/docs/7.x/installation) to ensure you have a working environment before continuing.

**Then, run the following command**:

```bash
npx use-preset laravel-inertia
```

By default, the preset installs the VILT stack. If you wish to not use Vue, you can use the `--no-vue` flag.

# Authentication scaffolding

The authentication system is copied into your project, so you don't need to use `laravel/ui`. Additionally, it uses the [Single Action Controller](https://driesvints.com/blog/the-beauty-of-single-action-controllers/) approach.

# Code-splitting

Code-splitting should be enabled if you have a large application. When code-splitting is used, it requires that the user download new assets as they navigate from one page to the next, which adds latency. When it is not, the first page load may take longer. This is a trade-off.

To enable code-splitting, uncomment the line in your `app.js` that makes `resolveComponent` use `import`, and remove the previous line. For more information, check out the [instructions](https://inertiajs.com/client-side-setup#code-splitting) on the Inertia documentation.

# To-do

- Add a React scaffolding (contributions welcome!)
- Add register, confirm password, reset password, send verification email, and verify email functionalities
- Organize Vue's authentication scaffolding into components
