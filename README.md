<p align="center">
  <img width="300px" src="https://user-images.githubusercontent.com/10731096/95823103-9ce15780-0d5f-11eb-8010-1bd1b5910d4f.png">
</p>

<p align="center">Element Plus - A Vue.js 3.0 UI library</p>

* 💪 Vue 3.0 Composition API
* 🔥 Written in TypeScript

This project is still under heavy development. Feel free to join us and make your first pull request.

[![Edit element-plus](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/element-plus-ncxnt?fontsize=14&hidenavigation=1&theme=dark)

---

Join our [Discord](https://discord.link/ElementPlus) to start communicating with everybody.

## Bootstrap project
With command
```bash
$ yarn bootstrap
```
the project will install all dependencies and run `lerna bootstrap` to initialize the project

## Website preview
With command
```bash
$ yarn website-dev
```
the project will launch website for you to preview all existing component

You can also use this command to start a blank page to debug
```bash
$ yarn website-dev:play
//source file: ./website/play/index.vue
```
## Component migration process
1. Convert the item in https://github.com/element-plus/element-plus/projects/1 to an issue
2. Assign yourself to the issue
3. Author your component by generating new component command below
4. Migrate tests and docs
5. Open a new pull request, fill in the component issue link in 1

## Generate new component
With command
```bash
$ yarn gen component-name
```

Note the `component-name` must be in `kebab-case`, combining words by replacing each space with a dash.

## Commit template
With command
```bash
yarn cz
```

Example
```
[TYPE](SCOPE):DESCRIPTION#[ISSUE]
# example feat(button):add type 'button' for form usage #1234
```

