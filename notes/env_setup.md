1. Install [NVM](https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating) to manage node versions.
```
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.0/install.sh | bash
```

2. NVM uses Node v12 by default, use the following commands to install and select desired node version (18 is LTS at time of writing this).
```
$ nvm install 16
$ nvm use 16
$ node -v
```

3. Install latest version of npm.
```
$ npm install -g npm
$ npm -v
```

4. Create a react projects using react's Next.js framework. Name the project, select yes to TypeScript and ESLint (static code analysis tool), Tailwind CSS is great as well! Using the src/ directory is useful, App Router is necessary and no need to customize import alias.
```
$ npx create-next-app@latest
```

**NOTE**
To just use TS with no react project, it can just be installed using ```npm install typescript --save-dev```.