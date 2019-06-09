# test-prlint

Repo to use when testing pr-lint.

PRLint checks that your PR abides by team conventions.

The root directory of your repo should contain a .prlint file.

The .prlint file should contain a field called `checks`.

The `checks` object may contain the following fields: `commit`, `pr`.

The `commit` object contains checks that should be performed on the commit that triggered the check.

The `pr` object contains checks that should be performed on the pull request that triggered the check.

Each check is a key-value pair where the key is the name of the check to perform and the value is the (JavaScript) script to be executed for that check.

If the script evaluates to true then the check passes. If not, the check fails.

The script can be either a string or an array of strings. If the script tag is a string it is expected to be an expression to be evaluated, not a return statement; i.e. it is not expected to have the return keyword. If the script tag is an array of
