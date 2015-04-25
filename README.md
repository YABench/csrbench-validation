# CSRBench-validation

A set of tests validating YABench framework against [CSRBench](https://github.com/dellaglio/csrbench-oracle-engines). Using this test one can check whether YABench produces the similar to CSRBench results.

## Preparing

First of all, you need to clone this repository, download the latest release of YABench framework from the [releases page](https://github.com/YABench/yabench/releases) and unpack it.

Make sure that you have installed all required software and dependencies which are listed in [Installing](https://github.com/YABench/yabench/wiki#installing) wiki page.

Now you're ready to run the tests!

## Running

Example of the command to execute a test:
```
./runner.py <test folder> -Dinputstream=<CSRBench's inputstream> -Dexec.oracle=<path to Oracle's .jar> -Dexec.engine=<path to Engine's jar>
```

In example, if you've unpacked the release archive to the cloned repository folder, so you have the following folder structure:
```
-- .
-- cqels_Q1/
-- cqels_Q2/
...
-- csparql_Q1/
...
-- yabench-<version>/
-- csrbench-inputstream.n3t
```

And you want to run test `cqels_Q1`, then you need to execute the following command:
```
./yabench-<version>/yabench-runner/runner.py cqels_Q1 -Dinputstream=csrbench-inputstream.n3t -Dexec.oracle=yabench-<version>/yabench-oracle.jar -Dexec.engine=yabench-<version>/yabench-cqels.jar
```

The results can be found in `cqels_Q1/results` folder.
