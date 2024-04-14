## How to setup talwind css for production ready app

step 1. run the following commands
initialise the nodejs app

```` 
npm init 
npm install -D tailwindcss
npx tailwindcss init
````

step 2. update your talwind.config.js file with this code to render your html files only

````
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["*.html"],
  theme: {
    extend: {},
  },
  plugins: [],
};

````

step 3. create your src/input.css file to include

````
@tailwind base;
@tailwind components;
@tailwind utilities;
````

step 4. connect the src/output.css file to your html files

step 5. run the following commands

````
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
````