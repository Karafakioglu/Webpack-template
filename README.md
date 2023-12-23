Run Dev Server (Port 3000)

```
npm run dev
```

Build for production

```
npm run build
```

In package.json you can change the following to whatever your project name is

```
"name": "webpack-template",
```

This is taken from
https://www.youtube.com/watch?v=IZGNcSuwBZs Webpack 5 Crash Course | Frontend Development Setup by Traversy Media

https://github.com/bradtraversy/webpack-starter/tree/main

<details>

<summary>How to upload to github pages</summary>

First, you need to install gh-pages package. This package will create a gh-pages branch on your repository and push your built files to this branch. You can install it using npm:

```
npm install gh-pages --save-dev
```

Then, you need to add a homepage field to your package.json. This field should point to the URL where your project will be hosted. The URL is usually in the format https://{username}.github.io/{repo}. For example:

```
"homepage": "http://myusername.github.io/my-app"
```

Next, add scripts to build your application and deploy it to GitHub Pages. In your package.json, add these lines:

```
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d dist"
}
```

The predeploy script will run automatically before deploy is run. It will build your application and put the built files in the dist directory. The deploy script will then push these files to the gh-pages branch of your repository.

Now, you can run npm run deploy to deploy your application to GitHub Pages.

Finally, go to the settings of your repository on GitHub, scroll down to the GitHub Pages section, and select gh-pages branch as your source. Your application should now be live at the URL you specified in the homepage field.

Remember to commit and push all your changes to your repository before running the deploy script.

Make sure that what you have here `"homepage": "http://myusername.github.io/my-app"` matches what you have in your GitHub repository because GitHub Pages uses the repository name as part of the URL for your hosted application.

</details>
