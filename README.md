# Test Utils Orb

<!---
[![CircleCI Build Status](https://circleci.com/gh/GovStackWorkingGroup/test-utils.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/GovStackWorkingGroup/test-utils) [![CircleCI Orb Version](https://badges.circleci.com/orbs/GovStackWorkingGroup/testutils.svg)](https://circleci.com/orbs/registry/orb/GovStackWorkingGroup/testutils) [![GitHub License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/GovStackWorkingGroup/test-utils/master/LICENSE) [![CircleCI Community](https://img.shields.io/badge/community-CircleCI%20Discuss-343434.svg)](https://discuss.circleci.com/c/ecosystem/orbs)

--->
Orb for attaching test harness execution to building block repositories. 

---

## Resources

[CircleCI Orb Registry Page](https://circleci.com/orbs/registry/orb/GovStackWorkingGroup/testutils) - The official registry page of this orb for all versions, executors, commands, and jobs described.

[CircleCI Orb Docs](https://circleci.com/docs/2.0/orb-intro/#section=configuration) - Docs for using, creating, and publishing CircleCI Orbs.

### How to Contribute

We welcome [issues](https://github.com/GovStackWorkingGroup/test-utils/issues) to and [pull requests](https://github.com/GovStackWorkingGroup/test-utils/pulls) against this repository!

### How to Publish An Update
1. Merge pull requests with desired changes to the main branch.
    - For the best experience, squash-and-merge and use [Conventional Commit Messages](https://conventionalcommits.org/).
2. Find the current version of the orb.
    - You can run `circleci orb info govstack-working-group/testutils | grep "Latest"` to see the current version.
3. Create a [new Release](https://github.com/GovStackWorkingGroup/test-utils/releases/new) on GitHub.
    - Click "Choose a tag" and _create_ a new [semantically versioned](http://semver.org/) tag. (ex: v1.0.0)
      - We will have an opportunity to change this before we publish if needed after the next step.
4.  Click _"+ Auto-generate release notes"_.
    - This will create a summary of all of the merged pull requests since the previous release.
    - If you have used _[Conventional Commit Messages](https://conventionalcommits.org/)_ it will be easy to determine what types of changes were made, allowing you to ensure the correct version tag is being published.
5. Now ensure the version tag selected is semantically accurate based on the changes included.
6. Click _"Publish Release"_.
    - This will push a new tag and trigger your publishing pipeline on CircleCI.

### Development and testing

When you create a feature branch and push commits to it, the orb will be published on Circle with a dev tag, which can be used for testing.

This tag will have the following form:

```
govstack-working-group/testutils@dev:<HASH>
```

You can find this tag in the logs of the `Publishing Orb Release` step of the `orb-tools/publish` job in the `lint-pack` pipeline.

When you find this tag, you can then use it in the Circle config of other building blocks on feature branches in order to test your changes.

**Important**: do not use dev versions of the orb on the main branch of any building block.

