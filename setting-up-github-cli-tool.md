# Setting up github CLI tool

Thursday, 01 February 2024. 17:21:27GMT

## Installing and setting gh cli up (20230422193618)

1. Install `gh` tool with `sudo pacman -S github-cli`
2. Enter `gh auth login`
   - Select `Github.com` option
   - Select `ssh` for preferred protocol (I've already set up ssh key authentication with my Github acount)
   - I choose to `Skip` uploading ssh key to Github as I've done it already.
   - Choose to `Paste an authentication token`. (Generated on Github's website in Settings > Developer Settings > Tokens (classic))
   - Login should be successful.
    
## Push existing project to a new github repo (20230422194014)

1. Go into the root folder of your project you want to push to Github.
2. Initialise as a git repository with `git init`
3. Enter `gh repo create`.
   - Choose `push an existing local repository to Github`.
   - Press enter on the default "`.`" option.
   - Enter a name for the repository on Github (will default to local project's folder name)
   - I had to select the `repository owner` as I'm a member of a number of Github organistions.
   - Add in a description for the repo.
   - Choose your repository visibility. I choose `public`.
   - I choose `Yes` to add a remote.
   - New remote I keep as being called `origin`.
4. The project should now have a new repository in your Github account.

