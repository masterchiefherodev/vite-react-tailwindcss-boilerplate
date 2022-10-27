## __Empty project preconfigured to use vite, react and tailwind__
```
project
│   README.md
|   .gitignore
|   index.html
|   pacaake.json
|   pacaake.lock.json
|   postcss.config.cjs
|   tailwind.config.cjs
|   vite.config.cjs
│   📁️node__modeles    
│
└───📁️public
|
└───📁️src
|   │   📁️assets
|   |   |  App.jsx
|   |   |  index.css
|   |   |  main.jsx

```

## __Docs__

[React + Vite](https://vitejs.dev/guide/)

[TailwindCss](https://tailwindcss.com/docs/guides/vite)

## 🛠️ __Do it yourself__

1. Create the project with vite
```
npm create vite@latest my-project -- --template react
cd my-project
```
2. Install Tailwind CSS
```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```
3. Configure your template paths (__in tailwind.config.cjs__)
~~~
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
~~~
4. Add the Tailwind directives to your CSS

Add the @tailwind directives for each of Tailwind’s layers to your ./src/index.css file.
~~~
@tailwind base;
@tailwind components;
@tailwind utilities;
~~~
5. Start your build process
~~~
npm run dev
~~~
6. Start using Tailwind in your project
~~~
export default function App() {
  return (
    <h1 className="text-3xl font-bold underline">
      Hello world!
    </h1>
  )
}
~~~
## [📖️ __original guide__](https://tailwindcss.com/docs/guides/vite)