# devenv.nix options

## enterShell
TODO

*_Type_*:
strings concatenated with "\n"


*_Default_*
```
""
```




## env
TODO

*_Type_*:
attribute set


*_Default_*
```
{}
```




## packages
TODO

*_Type_*:
list of package


*_Default_*
```
[]
```




## postgres.createDatabase
Create a database named like current user on startup.


*_Type_*:
boolean


*_Default_*
```
true
```




## postgres.enable
Whether to enable Add postgresql process and expose utilities..

*_Type_*:
boolean


*_Default_*
```
false
```


*_Example_*
```
true
```


## postgres.initdbArgs
Additional arguments passed to `initdb` during data dir
initialisation.


*_Type_*:
list of strings concatenated with "\n"


*_Default_*
```
["--no-locale"]
```


*_Example_*
```
["--data-checksums","--allow-group-access"]
```


## postgres.package
Which version of postgres to use

*_Type_*:
package


*_Default_*
```
"pkgs.postgresql"
```




## pre-commit
Integration of https://github.com/cachix/pre-commit-hooks.nix

*_Type_*:
submodule


*_Default_*
```
{}
```




## pre-commit.default_stages
A configuration wide option for the stages property.
Installs hooks to the defined stages.
See <link xlink:href="https://pre-commit.com/#confining-hooks-to-run-at-certain-stages"></link>.


*_Type_*:
list of string


*_Default_*
```
["commit"]
```




## pre-commit.excludes
Exclude files that were matched by these patterns.


*_Type_*:
list of string


*_Default_*
```
[]
```




## pre-commit.hooks
The hook definitions.

Pre-defined hooks can be enabled by, for example:

<programlisting language="nix">
hooks.nixpkgs-fmt.enable = true;
</programlisting>The pre-defined hooks are:

<emphasis role="strong"><literal>actionlint</literal></emphasis>

Static checker for GitHub Actions workflow files.

<emphasis role="strong"><literal>alejandra</literal></emphasis>

The Uncompromising Nix Code Formatter.

<emphasis role="strong"><literal>ansible-lint</literal></emphasis>

Ansible linter.

<emphasis role="strong"><literal>black</literal></emphasis>

The uncompromising Python code formatter.

<emphasis role="strong"><literal>brittany</literal></emphasis>

Haskell source code formatter.

<emphasis role="strong"><literal>cabal-fmt</literal></emphasis>

Format Cabal files

<emphasis role="strong"><literal>cabal2nix</literal></emphasis>

Run <literal>cabal2nix</literal> on all <literal>*.cabal</literal> files to generate corresponding <literal>default.nix</literal> files.

<emphasis role="strong"><literal>cargo-check</literal></emphasis>

Check the cargo package for errors.

<emphasis role="strong"><literal>chktex</literal></emphasis>

LaTeX semantic checker

<emphasis role="strong"><literal>clang-format</literal></emphasis>

Format your code using <literal>clang-format</literal>.

<emphasis role="strong"><literal>clippy</literal></emphasis>

Lint Rust code.

<emphasis role="strong"><literal>deadnix</literal></emphasis>

Scan Nix files for dead code (unused variable bindings).

<emphasis role="strong"><literal>dhall-format</literal></emphasis>

Dhall code formatter.

<emphasis role="strong"><literal>elm-format</literal></emphasis>

Format Elm files.

<emphasis role="strong"><literal>elm-review</literal></emphasis>

Analyzes Elm projects, to help find mistakes before your users find them.

<emphasis role="strong"><literal>elm-test</literal></emphasis>

Run unit tests and fuzz tests for Elm code.

<emphasis role="strong"><literal>eslint</literal></emphasis>

Find and fix problems in your JavaScript code.

<emphasis role="strong"><literal>fourmolu</literal></emphasis>

Haskell code prettifier.

<emphasis role="strong"><literal>govet</literal></emphasis>

Checks correctness of Go programs.

<emphasis role="strong"><literal>hadolint</literal></emphasis>

Dockerfile linter, validate inline bash.

<emphasis role="strong"><literal>hindent</literal></emphasis>

Haskell code prettifier.

<emphasis role="strong"><literal>hlint</literal></emphasis>

HLint gives suggestions on how to improve your source code.

<emphasis role="strong"><literal>hpack</literal></emphasis>

<literal>hpack</literal> converts package definitions in the hpack format (<literal>package.yaml</literal>) to Cabal files.

<emphasis role="strong"><literal>html-tidy</literal></emphasis>

HTML linter.

<emphasis role="strong"><literal>hunspell</literal></emphasis>

Spell checker and morphological analyzer.

<emphasis role="strong"><literal>isort</literal></emphasis>

A Python utility / library to sort imports.

<emphasis role="strong"><literal>latexindent</literal></emphasis>

Perl script to add indentation to LaTeX files.

<emphasis role="strong"><literal>luacheck</literal></emphasis>

A tool for linting and static analysis of Lua code.

<emphasis role="strong"><literal>markdownlint</literal></emphasis>

Style checker and linter for markdown files.

<emphasis role="strong"><literal>mdsh</literal></emphasis>

Markdown shell pre-processor.

<emphasis role="strong"><literal>nix-linter</literal></emphasis>

Linter for the Nix expression language.

<emphasis role="strong"><literal>nixfmt</literal></emphasis>

Nix code prettifier.

<emphasis role="strong"><literal>nixpkgs-fmt</literal></emphasis>

Nix code prettifier.

<emphasis role="strong"><literal>ormolu</literal></emphasis>

Haskell code prettifier.

<emphasis role="strong"><literal>prettier</literal></emphasis>

Opinionated multi-language code formatter.

<emphasis role="strong"><literal>purs-tidy</literal></emphasis>

Format purescript files.

<emphasis role="strong"><literal>purty</literal></emphasis>

Format purescript files.

<emphasis role="strong"><literal>revive</literal></emphasis>

A linter for Go source code.

<emphasis role="strong"><literal>rustfmt</literal></emphasis>

Format Rust code.

<emphasis role="strong"><literal>shellcheck</literal></emphasis>

Format shell files.

<emphasis role="strong"><literal>shfmt</literal></emphasis>

Format shell files.

<emphasis role="strong"><literal>statix</literal></emphasis>

Lints and suggestions for the Nix programming language.

<emphasis role="strong"><literal>stylish-haskell</literal></emphasis>

A simple Haskell code prettifier

<emphasis role="strong"><literal>stylua</literal></emphasis>

An Opinionated Lua Code Formatter.

<emphasis role="strong"><literal>terraform-format</literal></emphasis>

Format terraform (<literal>.tf</literal>) files.

<emphasis role="strong"><literal>yamllint</literal></emphasis>

Yaml linter.




*_Type_*:
attribute set of (submodule)


*_Default_*
```
{}
```




## pre-commit.hooks.\<name\>.description
Description of the hook. used for metadata purposes only.


*_Type_*:
string


*_Default_*
```
""
```




## pre-commit.hooks.\<name\>.enable
Whether to enable this pre-commit hook.

*_Type_*:
boolean


*_Default_*
```
false
```




## pre-commit.hooks.\<name\>.entry
The entry point - the executable to run. <option>entry</option> can also contain arguments that will not be overridden, such as <literal>entry = "autopep8 -i";</literal>.


*_Type_*:
string






## pre-commit.hooks.\<name\>.excludes
Exclude files that were matched by these patterns.


*_Type_*:
list of string


*_Default_*
```
[]
```




## pre-commit.hooks.\<name\>.files
The pattern of files to run on.


*_Type_*:
string


*_Default_*
```
""
```




## pre-commit.hooks.\<name\>.language
The language of the hook - tells pre-commit how to install the hook.


*_Type_*:
string


*_Default_*
```
"system"
```




## pre-commit.hooks.\<name\>.name
The name of the hook - shown during hook execution.


*_Type_*:
string


*_Default_*
```
{"_type":"literalDocBook","text":"internal name, same as id"}
```




## pre-commit.hooks.\<name\>.pass_filenames
Whether to pass filenames as arguments to the entry point.


*_Type_*:
boolean


*_Default_*
```
true
```




## pre-commit.hooks.\<name\>.raw
Raw fields of a pre-commit hook. This is mostly for internal use but
exposed in case you need to work around something.

Default: taken from the other hook options.


*_Type_*:
attribute set of unspecified value






## pre-commit.hooks.\<name\>.stages
Confines the hook to run at a particular stage.


*_Type_*:
list of string


*_Default_*
```
{"_type":"literalExpression","text":"default_stages"}
```




## pre-commit.hooks.\<name\>.types
List of file types to run on. See <link xlink:href="https://pre-commit.com/#plugins">Filtering files with types</link>.


*_Type_*:
list of string


*_Default_*
```
["file"]
```




## pre-commit.hooks.\<name\>.types_or
List of file types to run on, where only a single type needs to match.


*_Type_*:
list of string


*_Default_*
```
[]
```




## pre-commit.installationScript
A bash snippet that installs nix-pre-commit-hooks in the current directory


*_Type_*:
string






## pre-commit.package
The <literal>pre-commit</literal> package to use.


*_Type_*:
package


*_Default_*
```
{"_type":"literalExpression","text":"pkgs.pre-commit\n"}
```




## pre-commit.rootSrc
The source of the project to be checked.

This is used in the derivation that performs the check.

If you use the <literal>flakeModule</literal>, the default is <literal>self.outPath</literal>; the whole flake
sources.


*_Type_*:
path


*_Default_*
```
{"_type":"literalExpression","text":"gitignoreSource config.src"}
```




## pre-commit.run
A derivation that tests whether the pre-commit hooks run cleanly on
the entire project.


*_Type_*:
package


*_Default_*
```
"<derivation>"
```




## pre-commit.settings.alejandra.exclude
Files or directories to exclude from formatting.

*_Type_*:
list of string


*_Default_*
```
[]
```


*_Example_*
```
["flake.nix","./templates"]
```


## pre-commit.settings.deadnix.fix
Remove unused code and write to source file.

*_Type_*:
boolean


*_Default_*
```
false
```




## pre-commit.settings.deadnix.noLambdaArg
Don't check lambda parameter arguments.

*_Type_*:
boolean


*_Default_*
```
false
```




## pre-commit.settings.deadnix.noLambdaPatternNames
Don't check lambda pattern names (don't break nixpkgs <literal>callPackage</literal>).

*_Type_*:
boolean


*_Default_*
```
false
```




## pre-commit.settings.deadnix.noUnderscore
Don't check any bindings that start with a <literal>_</literal>.

*_Type_*:
boolean


*_Default_*
```
false
```




## pre-commit.settings.deadnix.quiet
Don't print a dead code report.

*_Type_*:
boolean


*_Default_*
```
false
```




## pre-commit.settings.eslint.binPath
<literal>eslint</literal> binary path. E.g. if you want to use the <literal>eslint</literal> in <literal>node_modules</literal>, use <literal>./node_modules/.bin/eslint</literal>.

*_Type_*:
path


*_Default_*
```
{"_type":"literalExpression","text":"${tools.eslint}/bin/eslint"}
```




## pre-commit.settings.eslint.extensions
The pattern of files to run on, see <link xlink:href="https://pre-commit.com/#hooks-files"></link>.

*_Type_*:
string


*_Default_*
```
"\\.js$"
```




## pre-commit.settings.hpack.silent
Whether generation should be silent.

*_Type_*:
boolean


*_Default_*
```
false
```




## pre-commit.settings.nix-linter.checks
Available checks. See <literal>nix-linter --help-for [CHECK]</literal> for more details.

*_Type_*:
list of string


*_Default_*
```
[]
```




## pre-commit.settings.ormolu.cabalDefaultExtensions
Use <literal>default-extensions</literal> from <literal>.cabal</literal> files.

*_Type_*:
boolean


*_Default_*
```
false
```




## pre-commit.settings.ormolu.defaultExtensions
Haskell language extensions to enable.

*_Type_*:
list of string


*_Default_*
```
[]
```




## pre-commit.settings.prettier.binPath
<literal>prettier</literal> binary path. E.g. if you want to use the <literal>prettier</literal> in <literal>node_modules</literal>, use <literal>./node_modules/.bin/prettier</literal>.

*_Type_*:
path


*_Default_*
```
{"_type":"literalExpression","text":"\"${tools.prettier}/bin/prettier\"\n"}
```




## pre-commit.settings.revive.configPath
Path to the configuration TOML file.

*_Type_*:
string


*_Default_*
```
""
```




## pre-commit.settings.statix.format
Error Output format.

*_Type_*:
one of "stderr", "errfmt", "json"


*_Default_*
```
"errfmt"
```




## pre-commit.settings.statix.ignore
Globs of file patterns to skip.

*_Type_*:
list of string


*_Default_*
```
[]
```


*_Example_*
```
["flake.nix","_*"]
```


## pre-commit.src
Root of the project. By default this will be filtered with the <literal>gitignoreSource</literal>
function later, unless <literal>rootSrc</literal> is specified.

If you use the <literal>flakeModule</literal>, the default is <literal>self.outPath</literal>; the whole flake
sources.


*_Type_*:
path






## pre-commit.tools
Tool set from which <literal>nix-pre-commit-hooks</literal> will pick binaries.

<literal>nix-pre-commit-hooks</literal> comes with its own set of packages for this purpose.


*_Type_*:
lazy attribute set of package


*_Default_*
```
{"_type":"literalExpression","text":"pre-commit-hooks.nix-pkgs.callPackage tools-dot-nix { inherit (pkgs) system; }"}
```




## processes
TODO

*_Type_*:
attribute set of (submodule)


*_Default_*
```
{}
```




## processes.\<name\>.exec
TODO

*_Type_*:
string






## scripts
TODO

*_Type_*:
attribute set of (submodule)


*_Default_*
```
{}
```




## scripts.\<name\>.exec
TODO

*_Type_*:
string





