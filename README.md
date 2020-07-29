# eslint-config-yathish
A one time setup for eslint and prettier settings without having to write the rules again and again

Step 1:  Add the dependencies in the working directory

```npx install-peerdeps --dev eslint-config-yathish```

Step 2: Using the eslint. Create a file named ".eslintrc" in the root of the project folder and the following it it.

```
{
  "extends": "yathish"
}
```

Step 3: Changing the setting of the VS code globally. Open File -> Preferences -> Settings. On the top right u can see the file icon click on that to open settings.json. Add the following code.

```// These are all my auto-save configs
"editor.formatOnSave": true,
// turn it off for JS and JSX, we will do this via eslint
"[javascript]": {
  "editor.formatOnSave": false
},
"[javascriptreact]": {
  "editor.formatOnSave": false
},
// tell the ESLint plugin to run on save
"editor.codeActionsOnSave": {
  "source.fixAll": true
},
// Optional BUT IMPORTANT: If you have the prettier extension enabled for other languages like CSS and HTML, turn it off for JS since we are doing it through Eslint already
"prettier.disableLanguages": ["javascript", "javascriptreact"],```

Step 3 is a one time thing to make the settings global. Repeat Step 1&2 for every project you like. And more importantly the rules can be added and deleted as needed.
