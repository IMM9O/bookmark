<h1 style="text-align: center;">Deployment</h1>
<p style="text-align: center;"> 
How to deploy your static website to "Static Web Host"
or how to exposing your local development to public url for demoing 
</p>



# Publish to Popular Platforms

- [GitHub Pages](https://pages.github.com/)
- [Firebase Hosting](https://firebase.google.com/docs/hosting)
- [netlify](https://www.netlify.com)
- [Vercel](https://vercel.com/)

## GitHub Pages

**How to use it ?**

1.  Install [gh-pages](https://github.com/tschaub/gh-pages) locally `npm install gh-pages --save-dev`
2.  Add new script to `package.json` file to deploy your website

```json
    "scripts": {
      // replase dist with your build dir folder
      "deploy": "gh-pages -d [dist]"
    }
    /*
     * Replace <username> and <repositoryname> with your username
     * from GitHub and the name of your new repository.
     */
    "home": "https://<username>.github.io/<repositoryname>/",
```

3.  Deploy your website to Github Pages by running this command `npm run deploy`

**Note**

`gh-pages` behind the scenes will create another branch called `gh-pages` to push your build files into it

## Firebase

1. You need to create new project first on [firebase console](https://console.firebase.google.com/)

2. Install `firebase-tools` package

```bash
$ npm install -g firebase-tools
```

3. Login to the account `firebase login`

4. Init firebase configuration for hosting `firebase init`

5. When your website ready just type `firebase deploy` 

## Netlify

**How to use it ?**

1. Create new account on [netlify](https://www.netlify.com)
2. Install [netlify-cli](https://www.netlify.com/products/dev/#how-it-works) globally `npm install netlify-cli -g`
3. login to your account from `netlify-cli` using this command `netlify login`
4. Inside your project folder genrate new website id for dpploy using this command `netlify init`
5. To deploy and make your website live use this command `netlify deploy --dir=dist --prod`

**Notes:**

The `deploy` command needs to know which folder to publish.
Netlify CLI will look for this information in three places, in
the following order:

1. in flags specified in the command itself `--dir=dist`.
2. in a netlify.toml file stored at the root of your project directory.
3. in your site settings in the Netlify UI.

```bash
# If you want to run your project on your local machine
$ netlify dev
# If you want to share it with your team
$ netlify dev --live
```




# Test Before publish
## Local Server

- [HTTP Server](https://github.com/http-party/http-server)
- [Live Server](https://github.com/tapio/live-server)
- [Webpack Dev Server](https://webpack.js.org/configuration/dev-server/)
- [BrowserSync](https://www.browsersync.io/)
- [Express](https://www.express.com/)

## Sharing work in progress

In case you want to expose your local server without worrying about deploy it on acutely server.

- [localtunnel](https://github.com/localtunnel/localtunnel)
- [ngrok](https://ngrok.com/)
- [Vercel](https://vercel.com/)
- [surge](https://surge.sh/)
- [netlify dev](https://www.netlify.com/products/dev/)

