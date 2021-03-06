##2013-10-28 - Scott Lee
 - Move to Haxe 3 and neko 2

##2013-08-01 - Yanhick, Richard, Todd
 - added many improvements to generated code style
 - replaced as3 "toString" by Haxe "Std.string"
 - replaced as3 "Date" by Haxe "Date.now" for current time
 - "callback" ident in as3 source replaced by "callbackfunc" because of Haxe reserved keyword
 - implemented support for as3 package level function, wrapped in Haxe class
 - replaced Haxe 2 "Hash" generation by Haxe 3 "Map"
 - removed comma before haxe "implements" keyword (haxe 3 syntax)
 - as3 "hasOwnProperty" replaced by haxe "exists"
 - replaced all tabs by spaces
 - Most newlines are now preserved from as3 source
 - Most comment are now preserved from as3 source
 - Added support for "final" as3 keyword
 - Added ENL type, representing source code new line chars
 - New line chars from as3 files are tokenised instead of ignored
 - Fixed bug where comment made semicolon appear on new lines
 - Class attribute can now be initialised inline
 - Implemented Haxe 3 getter/setter syntax
 - Removed writing var type in for(var x : String in y)
 - Created "in" as Binop : for(i in x)
 - Handle of if(x in y) as Lambda.has
 - Added handling for classes outside of package {} in as3 (private tail classes)
 - Removed conversion of escape sequences in Parser.readString
 - Added odd as3 vector constructor style: mStringVec = new <String>["a","b"];

##2011-10-19 - Russell
 - Added writing out class inits
 - Fixed empty functions returning f.expr = Object (messed up metadata parsing)
 - Improved metadata support for [Bindable("move")]
 - Added native flash getter and setter methods
 - Refactored configuration, reads xml config files
 - Fixed default values in function args
 - Fixed setters not returning values
 - Output Dynamic for Object
 - Added -no-func2dyn. Prevents Function type being changed to Dynamic
 - Total rewrite of Writer:ESwitch. Corrects switch..break behaviour of flash. See tests/Switch.as
 - Fixed isNaN -> Math.isNaN
 - Fixed continue statements in EFor blocks not incrementing counters. See tests/Loops.as
 - Type.getClass() for "as Class"
 - A little spaghetti, more copy pasta, and some casts to Stringozzi
 - Added compiler warnings
 - Fixed missed chars in token()
 - Parse typeof, added as3hx.Compat class to handle untranslatable flash
 - Skip comments in object create or fuction calls
 - Support for Vector added to Writer

##2011-10-14 - Russell
 - cleaned formatting on comments
 - added === support (missed)
 - added -no-cast-guess 

##2011-10-12 - Russell
 - added comments
 - fixed static var initializations were not output
 - added output for the "as" keyword
 - fixed "interface extends" to "interface implements" 
 - fixed interface functions were outputting empty bodies
 - added ETernary
 - fixed formatting on if...else
 - added parsing for !==
 - added -uint2int command line switch
 - fixed field access (none to never)
