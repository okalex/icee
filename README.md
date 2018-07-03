icee is an easy way to view and filter output from a running program, allowing you to see only what's important to you.

## Installation ##

Just copy `bin/icee` to somewhere on your `PATH`. If you wanna get real fancy, you can clone this repo and create a symlink to the executable.

```
$ git clone git@github.com:okalex/icee.git
$ chmod +x icee/bin/icee
$ ln -s $(pwd)/icee/bin/icee /usr/local/bin
```

## Usage ##

In one shell start your program with `icee run`. This will execute everything after `icee run`, displaying output and accepting input as normal.

```
$ icee run ./sbt runAllNow
```

 Then in another shell, you can view filtered output with `icee tail`.

 ```
 $ icee tail "crypto-server"
 ```

 This will display only lines that contain the text "crypto-server". Note that the argument to `icee tail` is a regex that's passed to `egrep`.

 ## To do ##

 - Add option so tail can display a certain number of lines after each match.
 