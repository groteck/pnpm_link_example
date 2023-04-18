# How to link local packages
This are instructions about how to link local packages

## Create 2 different projects

Creating the lib

```bash
mkdir lib_A
cd lib_A
pnpm init # use npm init if you don't want to use pnpm
```

```bash
mkdir project
cd project
pnpm init # use npm init if you don't want to use pnpm
```

## Now we need to link both projects

Now you do the link from the `project`

```bash
cd project
pnpm link ../lib_A # In this case we use the path ../lib_A because they are siblings but can be any path to the library

```

## Test the link checking the node_modles on the parent project
```bash
cd project
ls node_modules # => lib_A -> ../../lib_A
```
