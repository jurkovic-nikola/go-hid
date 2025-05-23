# Contributing

If you have an idea or feature request please open an [issue][1], even if you
don't have time to contribute!

## Making Changes

> [!NOTE]
> This guide assumes you have a functioning Go 1.17 (or later) installation.

To get started, [fork][2] this repository on GitHub and clone a working copy for
development:

```
$ git clone git@github.com:YOUR-USERNAME/go-hid.git
```

Once you have finished making changes, run tests by issuing:

```
$ go test ./...
```

Finally, commit your changes and create a [pull request][3] against the default
branch for review. At a minimum, there should be no test regressions and
additional tests should be added for new functionality.

## Making Releases

Making releases is automated by [GitHub Actions][4]. Releases are created from
the default branch; as such, tests should be passing at all times.

To make a release, perform the following:

1. Create a new section in [CHANGELOG.md][5] for the release, and move items
   from Unreleased to this section. Links should also be updated to point to the
   correct tags for comparison.

2. Commit outstanding changes by issuing:

   ```
   $ git commit -a -m "Release v<version>"
   ```

3. Push changes and verify the results of the [CI][6] workflow.

4. Create a release tag from the default branch by issuing:

   ```
   $ git tag -a -m "Release v<version>" v<version>
   ```

5. Push the release tag to the remote repository and verify the results of the
   [Release][7] workflow:

   ```
   $ git push origin --tags
   ```

## License

By contributing to this repository, you agree that your contributions will be
licensed under its Simplified BSD License.

[1]: https://github.com/sstallion/go-hid/issues
[2]: https://docs.github.com/en/github/getting-started-with-github/fork-a-repo
[3]: https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request
[4]: https://docs.github.com/en/actions
[5]: https://github.com/sstallion/go-hid/blob/master/CHANGELOG.md
[6]: https://github.com/sstallion/go-hid/actions/workflows/ci.yml
[7]: https://github.com/sstallion/go-hid/actions/workflows/release.yml
