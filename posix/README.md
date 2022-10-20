# Posix
Linux is an operating system, that relies on standards to ensure diversity to be compatible.

Many commands provide a similar interface because of that. Getting to know those patterns eases the learning curve on other commands.

## Structure

`base command`: 
```
ls
```
or
```
git
```

base command with detailed `help`: 
```
ls --help
```
or 
```
man ls
```

base command with an `argument`: 
```
ls <path>
```

base command with a `subcommand`: 
```
git add <path>
```

base command with an `option`: 
```
ls -l
```

base command multiple options: 
```
ls -la
```

base commaned with a subcommand with a `option argument`
```
git commit -m "commit message"
```

base command with a `full-text option`: 
```
ls --all
```

base command with two full-text options: 
```
ls --all --human-readable
```

base commaned with a subcommand with a `full-text option argument`
```
git commit --reuse-message=<commit>
```


Base Command with both a short option and a full-text option: 
```
ls -l --all
```


