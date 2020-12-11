This project is no longer maintained and replace by [WeTransfer-iOS-CI](https://github.com/WeTransfer/WeTransfer-iOS-CI/).

# Danger
WeTransfer Danger file. Used for checking PRs on iOS projects. This can be used together with [Danger](https://github.com/danger/danger). More info can be found here: [http://danger.systems](http://danger.systems/).

## Features

- File checks.
- Check if tests are updated when more than 20 lines are commited.
- Require a PR body of at least 3 lines when more than 10 lines of code are commited.
- Do a basic check to see if files are in sync with the Xcode project structure.
- Mark a PR as BIG when over 500 lines of code.
- Check for [WIP] in the title and WIP in the labels to mark a PR as Work In Progress.

## File checks
Checks for certain rules and warns if needed.
Some rules can be disabled by using `// danger:disable rule_name`.
 
### Rules:
- Check to see if any of the modified or added files contains a class which isn't indicated as final (`final_class`)
- Check for large files without any `// MARK:`
- Check for the usage of unowned self. We rather like to use weak self to be safe.
- Check for override methods which only implement super calls. These can be removed.
- Check for public properties or methods which aren't documented (`public_docs`)

## Questions and support
Reach out on Twitter [@twannl](https://twitter.com/twannl) or create an issue in this repo.

## License

WeTransfer's Dangerfile is released under an MIT license. See the [License](License) file for more information.
