# SASS

By default this component has a "core" theme.

This can be enhanced by a framework theme:

 * Default (default; own)
 * Bootstrap (bootstrap3)
 * Bootstrap OLD (bootstrap)

## Creating themes

Built-in themes should try to recognize if the framework variable is already available and if available overloads the 
Default theme variables with the framework variables. This ensures that a sass project that is already overloading the 
framework variables has a consistent widget.

The variable overload is as such:

 * Hardcoded/Standalone framework variables overload "Default" variables.
 * Predefined variables (framework is available) overload "Default"/"Standalone" variables.
 * Default variables are used.

Each theme includes "core" and the "Default" theme variables and if necessary replaces / enhances the variables. 

### Example: Make your own theme

	// overload default vars here...
	// i.e. $alertify-font-family: 'serif';
	
	@include 'default/variables';
	@include 'core';
	
	// do your own elemental stuff here...



