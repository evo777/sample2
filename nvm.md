## What it is
- A bash script you can install to your bash profile
- Lets you easily switch the version of Node linked to your `node` command
- Switches to a compatible version of NPM for that version of Node
- **Note that globally installed packages are NOT shared between the versions of Node. You'll have to reinstall your packages (see second link in Resources for an easy way to do this)

## Why you'd might want to use it
- If you're working on different projects on the same machine that are pegged to different versions of Node and need to be able to switch quickly between them.

## How to install
1. Run `curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.1/install.sh | bash` 
2. Verify install with `command -v nvm`. Output should simply be 'nvm'
 - Try `source ~/.bash_profile` if it didn't work
3. Detailed instructions [here](https://github.com/creationix/nvm)

## How to use it (tldr version)
- Install a version of Node you'd like to have available
  - `nvm install 4.0`
- Switch to that version
  - `nvm use 4.0`
- Switch back to the normally installed version Node when you're done
  - `nvm use system`

## Resources
- https://github.com/creationix/nvm
- https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/
