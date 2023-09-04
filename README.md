# Developer Notes

This is the main repo for my developer-related notes. It contains submodules for each set of notes I have on GitHub.

This is mainly for myself but feel free to use these if you find them useful.

- Some of these notes were generated with the help of ChatGPT and AI tools.
- Where available, sources are listed in resources / references sections of the notes.

## How to use Git Submodules

### Add Submodules to Main Repo

```bash
git submodule add <URL_OF_SUBMODULE_REPO> <path/to/submodule>
```

### Working with Submodules

```bash
cd path/to/submodule

# Make changes, commit, and push in the submodule
# Work with the submodule just like any other Git repo
git add .
git commit -m "Updated notes for <language>"
git push
```

### Updating and Committing Changes to Submodules in Main Repo

**NOTE:** Need to be in the main repo's root directory

After making changes to a sub-module (and committing / pushing them), cd into root of main repo and run the following to update the main repo

```bash
# Fetch latest commits from the submodule repositories
# and update main repo to point to them
git submodule update --remote --merge
```

```bash
# Add the submodule changes
git add path/to/submodule

# Commit the changes
git commit -m "Updated submodule to latest version"

# Push changes to main repo
git push
```

### Cloning the Main Repository with Submodules

```bash
git clone <URL_OF_MAIN_REPO>
cd <main-notes-repo>
git submodule init
git submodule update
```
