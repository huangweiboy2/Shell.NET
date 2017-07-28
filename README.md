# Shell.NET [![License][License]](LICENSE.md) [![Build Status](https://travis-ci.org/phil-harmoniq/Shell.NET.svg?branch=master)](https://travis-ci.org/phil-harmoniq/Shell.NET)

[License]: https://img.shields.io/badge/License-MIT-blue.svg

Interact directly with the Bash shell in C#.

## Example

```C#
var bash = new Bash();
bash.Command("echo 'Some cool text' >> ~/Desktop/shell.net");
bash.Command("grep 'cool text' -nrH ~/Desktop");
bash.Command("grep 'cool text' -nrH ~/Desktop", redirect: true);
Console.WriteLine(bash.Output);
Console.WriteLine(bash.ExitCode);
```

## Details

Using the optional 'redirect' parameter will hide the output of commands and store it in `Bash.Output` and `Bash.ErrorMsg`. `Bash.ExitCode` will store the exit code of any command made.
