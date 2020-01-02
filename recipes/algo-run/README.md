# algo-run

This is a recipe for algorithmic programming contestants to run their programs with ease in common languages supported by online judeges (mainly [USACO](http://www.usaco.org/index.php?page=instructions/)). 

## Setup

Make sure you have `dunner` and `docker`. 

Run the following command to get the recipe
```
$ dunner init algo-run
```

This recipe creates a dunner task file `.dunner.yml`. Then you're good to go. 

## Usage

The following languages are supported:

### Python 2.7

```
$ dunner do python27 <file_name>
```
This will run `<file_name>.py` with Python2.7

### Python3.4
```
$ dunner do python34 <file_name>
```
This will run `<file_name>.py` with Python3.4

### Free Pascal Compilter 2.6.2
```
$ dunner do fpc <file_name>
```
This will compile `<file_name>.pas` and then execute `./<file_name>`

### gcc 4.8
```
$ dunner do gcc <file_name>
```
This will run `gcc -O2 -lm <file_name>.c -o <file_name>` and then execute `./<file_name>`

### g++ 4.8
```
$ dunner do g++ <file_name>
```
This will run `g++ -O2 -lm -std=c++0x <file_name>.cpp -o <file_name>` and then execute `./<file_name>`

## Extra
I also added the following just for convenience. 

### Python 3.7

```
$ dunner do python37 <file_name>
```
This will run `<file_name>.py` with Python3.7

### Python3.8
```
$ dunner do python38 <file_name>
```
This will run `<file_name>.py` with Python3.8