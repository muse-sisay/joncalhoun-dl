# joncalhoun-dl 🔥⬇

Downloads Go tutorial videos from <https://courses.calhoun.io>

> **Before you proceed, note that you must be a paid user for the paid content to download**

Kindly create your account [here](https://courses.calhoun.io/signup?). Jon is a great teacher, consider buying his premium courses if you want to.

## Installation

+ Ensure [youtube-dl](https://github.com/ytdl-org/youtube-dl#installation) is installed and in your PATH.

To install this package run

```bash
    $ go get -u github.com/timolinn/joncalhoun-dl
```

### To build from source run

```bash
    $ git clone git@github.com:timolinn/joncalhoun-dl.git
    $ cd joncalhoun-dl
    $ go build .
```

## How to use

If you installed via `go get`, you can simply run

```bash
    $ joncalhoun-dl -email=jon@doe.com -password=12345 -course=gophercises -output=your-chosen-directory
     [courses.calhoun.io]: fetching video urls for gophercises
     [courses.calhoun.io]: fetching data from https://courses.calhoun.io/courses/cor_gophercises...
```

If you built from source, the compiled binary should be in the current folder.

```bash
    $ ./joncalhoun-dl -email=jon@doe.com -password=12345 -course=gophercises -output=your-chosen-directory
     [courses.calhoun.io]: fetching video urls for gophercises
     [courses.calhoun.io]: fetching data from https://courses.calhoun.io/courses/cor_gophercises...
```

Also note, video downloads **resumes** from where it stopped, so should you experience network interruption nothing to worry about just make sure the output directory remains the same.

### Command [OPTIONS]

+ `--email` : Your account email address. Sign up [here](https://courses.calhoun.io/signup?)
+ `--password` : Your account password. _Unlike the unix password prompt, this will not hide your password by default, you'll have to keep an eye over your shoulder 😉_
+ `--course` : This is the name of the course you want to download. **Defaults** to `"gophercises"`
+ `--output` : This is the location directory you want the videos to be saved. It must be an absolute path. If this is not specified, we will try to create a `"/[course] folder"` (ie. the specified course name eg. `gophercises`) within your current working directory.

### Supported courses

+ [x] [gophercises](https://courses.calhoun.io/courses/cor_gophercises)
+ [x] [testwithgo](https://courses.calhoun.io/courses/cor_test)
+ [x] [webdevwithgo](https://courses.calhoun.io/courses/cor_webdev)
+ [ ] [advancedwebdevwithgo](https://https://courses.calhoun.io/courses/cor_awd)
+ [ ] [algorithms](https://courses.calhoun.io/courses/cor_algo)

### Contributing

There is still a couple features to implement, check the TODO list below.

+ Start by forking this repo
+ Create your branch
+ Implement your fixes, changes etc.
+ Open a Pull Request

### Issues

If you find a bug please create an [issue](https://github.com/timolinn/joncalhoun-dl/issues/new)

### Tests

To run existing tests

```bash
    $ go test
```

## TODO

+ [x] Add caching for requests
+ [x] Add default output directory
+ [x] Add output directoy flag
+ [x] provide packaged release
+ [ ] Add more unit tests
+ [ ] check for authentication error
+ [ ] prevent signin when using cache
+ [ ] choose video quality

### Authors

+ Timothy Onyiuke - _([github](https://github.com/timolinn), [twitter](https://twitter.com/timolinn_))_
+ Damilare Lana - _([github](https://github.com/damilarelana))_

If you find this repository to be of any help, please consider giving it Star! 🔥
