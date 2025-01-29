
# Generate Test Report with Autotools

Generate test reports based on [autotools](https://www.gnu.org/software/automake/manual/html_node/GNU-Build-System.html)
test suites.

This action generates a test report and outputs it as a
[job summary](https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/workflow-commands-for-github-actions#adding-a-job-summary).


## Usage

```yml
steps:
  - uses: actions/checkout@v4

  - name: Make all
    run: autoreconf --install; ./configure ; make all

  - if: success() || failure()
    uses: guillermocalvo/autotools-test-report@v1
```
