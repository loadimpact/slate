# Pull Requests

We love pull requests. Here's a quick guide:

1. Fork the repo.

2. Commit your changes. Please use 'docs' commit prefix and mentioned resource name in it.
If your pull request fixes an issue specify it in the commit message. Some examples:

  ```
  [docs] Update CONTRIBUTING.md for commit prefixes
  [user-scenarios/docs] add create spec
  ```

3. Push to your fork and submit a pull request. Please provide us with some
explanation of why you made the changes you made. 
We try to be quick about responding to tickets but sometimes we get a bit
backlogged.


Inline Documentation Guidelines:

All inline documentation is written in Markdown (Slate syntax). Follow these rules when
updating or writing new documentation:

1. Layout data must be defined in `source/index.html.md` file
2. Resource docs files must be defined in `source/includes` folder. Example `source/includes/_user-scenarios.html.md`
3. Use separate files for different resources.
4. When defining new resources follow the structure defined in `source/incudes/_pattern.html.md' file

NOTE: Partially copied from https://raw.githubusercontent.com/emberjs/ember.js/master/CONTRIBUTING.md
