# heroku-buildpack-github-npmrc
Heroku buildpack for overriding the .npmrc file in the build directory for authorization with npm when installing our private packages.

Add the buildpack to your Heroku app either using the CLI or the Heroku dashboard. 
The buildpack should run before any other buildpacks using npm, e.g:
```bash
$ heroku buildpacks:set --index 1 https://github.com/digital-advisor/heroku-buildpack-github-npmrc.git
$ heroku buildpacks:add heroku/nodejs
```

## Configure Config Var
Add the GITHUB_AUTH_TOKEN env in Heroku.

``` bash
 $ heroku config:set GITHUB_AUTH_TOKEN=00000000-0000-0000-0000-000000000000
```
