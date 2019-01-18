The file `main.workflow` isn't where I expected. Here are some troubleshooting steps that might help.

| Problem                                                     | Solution                                                                                                                                                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| The file isn't called `main.workflow` (case sensitive)      | Rename the file using the [UI](https://help.github.com/articles/renaming-a-file/) or [your CLI](https://help.github.com/articles/renaming-a-file-using-the-command-line/)                       |
| The directory `.github` doesn't exist.                      | [Create the `.github` folder](https://help.github.com/articles/creating-new-files/) and [move `main.workflow`](https://help.github.com/articles/moving-a-file-to-a-new-location/) to `.github`. |
| The `main.workflow` file isn't inside the `.github` folder. | [Move `main.workflow`](https://help.github.com/articles/moving-a-file-to-a-new-location/) to `.github`.                                                                                         |

I'll respond when you push to this branch. 