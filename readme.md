# TEST-NPM-INSTALL

This module is here simply to aid in the testing of the `npm install` command when used inside modules.

## How to use

### npm install <from npm>

```
require("child_process").exec("npm install test-npm-install", function(err){
	if(err){
		throw err;
	}
	else{
		require("test-npm-install");
	}
});
```

### npm install <from url>

```
require("child_process").exec("npm install https://github.com/mcwhittemore/test-npm-install/tarball/master", function(err){
	if(err){
		throw err;
	}
	else{
		require("test-npm-install");
	}
});
```

### npm install <local>

```
require("child_process").exec("npm install ./path/to/test-npm-install", function(err){
	if(err){
		throw err;
	}
	else{
		require("test-npm-install");
	}
});
```