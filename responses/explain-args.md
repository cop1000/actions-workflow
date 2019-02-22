By filling in the `args` field, you're passing arguments to the action, which is running in a Docker container. 

In this case, we passed in arguments with the `-e` option. This allows us to set environment variables in Zeit Now. 

When an action runs, some [environment variables are set by GitHub](https://developer.github.com/actions/creating-github-actions/accessing-the-runtime-environment/#environment-variables) and available in the runtime environment. Although these are available in the Docker container, they need to be explicitly passed to Zeit Now if we want our deployed application to make use of them. 

Get your deployment URL by going into the Actions tab. You can then visit it to examine the newly deployed app. You'll see that it now looks something like this:

![screenshot of deployed web app with confetti](https://user-images.githubusercontent.com/16547949/52747405-b1c97e80-2fb1-11e9-924c-70fb3a37ce14.png)