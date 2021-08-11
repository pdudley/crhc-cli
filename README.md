# C.RH.C API Command Line Tool

This project contains the `crhc` command line tool that simplifies the use of the C.RH.C API available at `console.redhat.com`

## Table of Content
 - [link](#Binary_File) - You can download the binary file
 - [link](#Source_Code) - You can clone the repository and use from the source code
 - [link](#Usage) - Usage
 - [link](#Contribution) - Contribution
 
---

## Binary_File
Please, access the release page [here](https://github.com/C-RH-C/crhc-cli/releases/latest) and check the version that you would like to use.

## Source_Code
Please, proceed with the steps below

In your RHEL/CentOS/Fedora/etc with Python 3.x installed, let's execute the commands in a sequence
```
$ git clone https://github.com/C-RH-C/crhc-cli.git
$ cd crhc-cli
$ python3 -m venv ~/.virtualenv/crhc-cli
$ source ~/.virtualenv/crhc-cli/bin/activate
```

Now, you should be in your virtual environment. You can realize your prompt will change
```
(crhc-cli) [user@server crhc-cli]$
```

We can continue
```
(crhc-cli) [user@server crhc-cli]$ pip install --upgrade pip
(crhc-cli) [user@server crhc-cli]$ pip install -r requirements.txt
```

And finally, we are good to go.
```
(crhc-cli) [user@server crhc-cli]$ ./crhc.py
```

The menu will be as below
```
(crhc-cli) [user@server crhc-cli]$ ./crhc.py 
Command line tool for console.redhat.com API

Usage:
  crhc [command]

Available Commands:
  inventory
  swatch

  user

Flags:
  -h, --help                         help for crhc

Use "crhc [command] --help" for more information about a command.
```



## Usage

The main idea of this script is to collect the information from `console.redhat.com` in order to generate some reports and/or proceed with some troubleshooting. That said, we can:

- `crhc user set` - To set the credentials that will be used to authenticate on console.redhat.com
- `crhc inventory list` - To list the first 50 entries of your RHEL Inventory
- `crhc inventory list_all` - To list all the entries of your RHEL Inventory
- `crhc inventory --display_name` - To search in RHEL Inventory by `display_name`
- `crhc swatch list` - To list the first 100 entries of your Subscription Watch Inventory
- `crhc swatch list_all` - To list all the entries of your Subscription Watch Inventory

Note. All of them will generate the output in a `JSON` format, so you can use the output as input for any of your own script or also to `jq` command.

## Contribution

I really hope this helps you.

If you need anything else of if you are facing issues trying to use it, please let me know via email or feel free to open a repository issue [here](https://github.com/C-RH-C/crhc-cli/issues)

waldirio@redhat.com / waldirio@gmail.com