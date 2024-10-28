# Nuxt Minimal Starter

Look at the [Nuxt documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

## Setup

Make sure to install dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm dev

# yarn
yarn dev

# bun
bun run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm build

# yarn
yarn build

# bun
bun run build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm preview

# yarn
yarn preview

# bun
bun run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
根目录文件
package.json：项目的核心配置文件，包含项目依赖、脚本（如 dev、build）、项目元信息等。npm run dev、npm run build 等命令都是在这里定义的。
npm run dev 是用于开发模式，便于调试和实时预览应用。
npm run build 是用于生产模式，生成最终的应用版本，优化和准备部署。

nuxt.config.js：Nuxt.js 的配置文件，控制项目的配置项（如路由、插件、模块、全局 CSS、环境变量等）。
.nuxt/：这是 Nuxt.js 的自动生成文件夹，通常在构建或运行开发服务器时生成，包含 Nuxt.js 内部使用的文件。注意： 此文件夹不需要手动编辑，且一般在 .gitignore 中被忽略。

核心目录
pages/：这是项目中页面的文件夹。Nuxt.js 会自动基于该目录中的文件生成路由。每个 .vue 文件都是一个页面组件。

例如：pages/index.vue 对应于根路径 /，pages/about.vue 对应于 /about。
layouts/：用于定义页面的布局文件。布局通常包含头部、导航栏、侧边栏等通用结构。每个页面可以选择一个布局文件。

例如：layouts/default.vue 为默认布局，页面中可以指定 layout: 'default' 使用它。
components/：组件目录，用于存放页面中可复用的 Vue 组件，例如按钮、表单等。与 pages/ 目录不同，components/ 中的组件不会自动生成路由，需要手动引入到页面中使用。

static/：用于存放静态资源（如图像、字体等）。其中的文件不会被编译，可以直接通过根路径访问。

例如：static/logo.png 可以通过 /logo.png 访问。
assets/：该目录用于存放需要 Webpack 处理的静态资源，如未编译的 SCSS、LESS 文件或图片。与 static/ 不同，assets/ 中的文件会被 Nuxt.js 的构建过程编译和优化。

middleware/：用于存放中间件函数，处理页面或路由进入前的操作。可以在路由或页面中定义一些前置逻辑，如用户认证检查。

store/：用于存放 Vuex 的状态管理文件。Nuxt.js 会自动读取该目录，并配置 Vuex。一般用于管理全局状态，如用户信息、设置等。

plugins/：用于存放需要在 Vue 实例化之前运行的 JavaScript 插件文件，比如在应用启动时加载第三方插件或注册全局组件。

composables/：用于存放组合式函数（适用于 Nuxt 3），这里的函数可以在整个应用中使用，便于组织和复用逻辑。
