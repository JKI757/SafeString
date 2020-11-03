# SafeString
This SafeString library is designed for beginners to be a safe, robust and debuggable replacement for string processing in Arduino.

# How-To
See [here](https://www.forward.com.au/pfod/ArduinoProgramming/SafeString/index.html).

# Note
Note, this is NOT my work, I am simply hosting it for easy access. The original code belongs to [Forward Computing and Control Pty. Ltd](https://www.forward.com.au/pfod/ArduinoProgramming/SafeString/index.html).

Note:

The original version of this library cannot be declared in a class and used as a private class member, due to the way the createSafeString macro works, and due to the fact that it has no constructor that allows it to be created with no arguments.

This updated version allows for declaration of a safestring as a private class member, and then initialization of said safestring in a class constructor.  This allows the object to be used throughout the class.

example declaration of a safestring named "name_line" with a length of 254 characters:

in .h private section:
    char name_line_SAFEBUFFER[254+1];
    SafeString name_line;
   
in constructor .cpp:
    name_line.init(254, name_line_SAFEBUFFER, "", "name_line");

