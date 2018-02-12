# submodule-test

#### Notes
- `config/locales` folder did not exist before
- Adding a submodule by `git submodule add git@github.com:Helpling/locales.git config/locales`
  - Git credentials were required
  - Some old git versions may require `git submodule update --init --recursive` to get the latest version.

## Initial setup
### git clone
When working on a project which uses sub modules, there are additional commands to be executed to get the content of the sub modules:
```bash
git clone git@github.com:Helpling/submodule-test.git
git submodule init
git submodule update
```
or simply
```bash
git clone --recurse-submodules git@github.com:Helpling/submodule-test.git
```
#### Already cloned repos or old Git versions (< 1.6.5)
git clone git@github.com:Helpling/submodule-test.git
git submodule update --init --recursive

## Updates
Run `git submodule update --remote` to get latest updates. This command will by default assume that you want to update the checkout to the master branch of the submodule repository.

#### Note
- A `git pull` on the main project won't get the latest commits from the submodule

## Resources
- [Working with submodules](https://github.com/blog/2104-working-with-submodules)
- [Git Tools - Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules)
- [How to `git clone` including submodules?](https://stackoverflow.com/questions/3796927/how-to-git-clone-including-submodules)
