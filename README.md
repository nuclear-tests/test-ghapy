# test-prlint

Repo to use when testing pr-lint.

PRLint checks that your PR abides by team conventions.

The root directory of your repo should contain a .prlint file.

The .prlint file should contain a field called `checks`.

The `checks` object may contain the following fields: `commit`, `pr`.

The `commit` object contains checks that should be performed on the commit that triggered the check.

The `pr` object contains checks that should be performed on the pull request that triggered the check.
