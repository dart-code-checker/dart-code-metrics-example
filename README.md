# Dart Code Metrics Flutter app example

This example demonstrates how Dart Code Metics can be set up for a Flutter project.

## Configuration

Dart Code Metrics configuration is listed in `analysis_options.yaml` file. [Check it out](analysis_options.yaml) for more details.

## Commands

You can find more details about the commands [on our website](https://dartcodemetrics.dev/docs/cli).

### Analyze

`Analyze` command is used to get a report about code metrics, rules and anti-patterns violations.

To execute the command, run

```sh
$ flutter pub run dart_code_metrics:metrics analyze lib test
```

### Check unused files

`Check unused files` command helps find files that are not referenced by any other file and are not a project entry point.
Such files are considered unused and are great candidates for complete removal since maintaining then most likely is an additional burden with no benefit.

To execute the command, run

```sh
$ flutter pub run dart_code_metrics:metrics check-unused-files lib
```

### Check unused code

`Check unused code` command helps find top-level declarations (like classes, functions, variables, etc.) that are not referenced by other code.
Such declarations are considered unused and are great candidates for complete removal since maintaining then most likely is an additional burden with no benefit.

If the code should be actually used, that's a great indicator that something went wrong and you have a potential bug in your code.

To execute the command, run

```sh
$ flutter pub run dart_code_metrics:metrics check-unused-code lib
```

### Check unnecessary nullable parameters

`Check unnecessary nullable` command helps find functions, methods and constructors parameters that currently marked as nullable, but there are no usages in the codebase with a nullable value, thus allowing to make parameter non-nullable.

To execute the command, run

```sh
$ flutter pub run dart_code_metrics:metrics check-unnecessary-nullable lib
```
