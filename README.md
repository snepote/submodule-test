# submodule-test

### Note
- `config/locales` folder did not exist before
- Adding a submodule by `git submodule add git@github.com:Helpling/locales.git config/locales`
  - Git credentials were required
  - Some old git versions may require `git submodule update --init --recursive` to get the latest version.

## Initial setup
### git clone
When working on a project which uses sub modules, there are additional commands to be executed to get
the content of the sub modules.
Either
- `git clone --recurse-submodules [MAIN_REPO]`
of
- `git clone [MAIN_REPO]`, then `git submodule init` and finally `git submodule update`

## Updates
Run `git submodule update --remote` to get latest updates. This command will by default assume that you want to update the checkout to the master branch of the submodule repository.

### Note
- A `git pull` on the main project won't get the latest commits from the submodule
