# Tailwind Integration

# How to install tailwind

open terminal and run below commands
`npm init -y` to create package.json file
`npm install -D tailwindcss` to install tailwind
`npx tailwindcss init` to create and initialize tailwind config file

Update the tailwind.config.js config file to include what file you need to compile

```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

# Import tailwind styles

create new file input.css and import below styles

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

now generate output.css file by running below commands

`npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch`

create index.html file and import output.css

# How to run

1. install `http-server` by running `npm i http-server -g`
2. open terminal and run `http-server`
3. launch `http://127.0.0.1:8080/src/index.html`

# Verification

open dist/output.css you would see whatever classes you've used in html file only those styles is being compiled and added to output.css file
