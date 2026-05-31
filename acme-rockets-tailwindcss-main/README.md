# Acme Rockets - Tailwind project

This repository hosts the codebase for Acme Rockets, a simple static website implementing Tailwind CSS and following CSS best practices. The website is deployed on render.com and can be accessed at https://a-rockets.onrender.com. 

## Get started with Tailwind CSS

- Initialize a project with npm.
```bash
npm init -y
```

- Install Tailwind CSS as a dev dependency.
```bash
npm install -D tailwindcss@latest
```

- Initialize a project with Tailwind CSS and create your 'tailwind.config.js'.
```bash
npx tailwindcss init
```

- Modify the tailwind.config.js file to include the paths of your CSS and JS files in the "content" property:
```js
content: ["./build/*.html", "./build/js/*.js"],
```

- Add the Tailwind directives to your CSS file. Create an 'input.css' file in the 'src' folder and include the following directives:.
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

 In some cases, you might encounter the error "unknown at-rule @tailwind" in VSCode. To resolve this, either modify the VSCode settings to avoid errors for future projects or add a '.vscode/settings.json' file with the following code (https://stackoverflow.com/questions/65247279/unknown-at-rule-tailwind-cssunknownatrules):
```json
{
  "files.associations": {
    "*.css": "tailwindcss"
  }
}
```
- Add a script in the 'package.json' to compile the CSS file. Run the command "npm run tailwind" in a dedicated terminal to generate the CSS file in the 'build/css' folder:
```json
"tailwind": "npx tailwindcss -i ./src/input.css -o ./build/css/style.css --watch"
```

## Topics covered

1. Class names, logic and using Emmet to speed up the process.
2. Responsive design - breakpoints - media queries.
3. Light & Dark mode depending on the user's preferences.
4. Hamburger menu with Html symbols or Pseudo elements (before, after) for better accessibility and animation.
5. Custom classes & arbitrary values + extend and override tailwind classes with custom classes (see tailwind.config.js).
6. Css config for sections full height depending on the viewport !!
7. Prettier plugin for tailwindcss. (npm install -D prettier-plugin-tailwindcss)
8. Deployement on render.com (https://a-rockets.onrender.com).