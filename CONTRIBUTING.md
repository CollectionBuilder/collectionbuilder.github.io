# How to Contribute to CollectionBuilder

Thank you for contributing to CollectionBuilder!

CollectionBuilder prioritizes pragmatic, sustainable, and simplified approaches to infrastructure to ensure the tool is "do-able" and approachable for digital knowledge workers in libraries and museums, empowering them to take control of their web systems. 
Much of the core team is *not* full time developers.
Thus, we are focused on creating a supportive, inclusive community with low barriers to contributing (please see our [Code of Conduct](https://github.com/CollectionBuilder/collectionbuilder.github.io/blob/master/CODE_OF_CONDUCT.md)).

Honestly, we do a lot of stuff the slow/old/inefficient/wrong way... but we make it work and invite you to learn/teach with us!

## Project resources

- Email contact: libstatic.uidaho@gmail.com 
- Main project site: <https://collectionbuilder.github.io/>
- User Documentation is found via the [CollectionBuilder home page](https://collectionbuilder.github.io/)
- Technical Documentation is found in individual project repositories in the "/docs" folder.
- General project tracking takes place in Issues in individual repositories, or the [CollectionBuilder home repository](https://github.com/CollectionBuilder/collectionbuilder.github.io/issues)

## Issues

Since this is a relatively small project, we are informal in using GitHub Issues. 
Issues should be opened in the specific repository for bug reports, feature ideas, and requests for missing documentation.
The team also uses Issues for project management related to the CollectionBuilder project.
Please focus on clear communication, providing plenty of detail so that we can understand the bug or proposal.
Always search Issues to see if a related report has already been opened (if so add a comment or reaction!).

However, if you encounter problems using the CollectionBuilder templates to build a personal collection, please check our [documentation](https://collectionbuilder.github.io/) resources for solutions and other ways to get in touch. 
Issues opened in CollectionBuilder repositories should be related to bugs and development problems in the central templates, *not* problems debugging personal metadata and pages. 
You don't need to open an Issue to ask a question, checkout our help and contact options!

- [GitHub Issues](https://guides.github.com/features/issues/)

## Pull Requests 

CollectionBuilder welcomes [Pull Requests](https://help.github.com/en/articles/about-pull-requests) from outside contributors. 
Please provide plenty of detail in the PR so that the project team fully understands your contribution.

- [How to create a PR](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)

## Conventions

- Include lots of inline comments documenting code! The entire project has a educational outlook.
- Include spaces for readability. For example, in Liquid `{% if site.example %}{{ site.example }}{% endif %}`, not `{%if site.example%}{{site.example}}{%endif%}`.
- To improve readability, avoid excess white space and random indentations.
- Indent using spaces. HTML, JS, CSS and related files should be indented using 4 spaces. YAML with 2 spaces.
- Main/master branch should be code that is ready to go. Use feature branches for development.
- Use `;` in metadata to denote multi-valued fields.
- New features should be progressive--adding features, while maintaining backwards compatibility with existing data setups. If possible, sane defaults should be set in Liquid, so that projects lacking updated config variables will still function.
