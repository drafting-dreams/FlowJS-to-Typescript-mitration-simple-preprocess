# Introduction

TS-Migrator is a helper tool to do some simple and repeating works when migrating FlowJS to TypeScript.

# Instructions

For linux based machines, create a file in /usr/local/bin and name it what ever you want, the file name will be the command name you're going to use. I'll just suppose the name is ts-migrator .

Currently, there're only two mode, normal mode and recursive mode.

For normal mode, run command `ts-migrator` in the directory you are going to migrate, it will do

Use git mv to rename all the files ending with 'js' or 'jsx' extension in the current directory, but it will ignore test files ending with '.test.js'
Delete comments `// @flow` and `// $FlowFixMe`
For recursive mode, attach -r after the command, it will do the same things in the normal mode, but recursively apply to all the sub directory under the current directory.

1. `ts-migrator` Migrate all files in the current folder
2. `ts-migrator -r` Migrate all files under the current folder recursively
3. `ts-migrator index.js` Migrate 'index.js' in the current folder
