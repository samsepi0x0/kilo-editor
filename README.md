# kilo-editor
An implementation of the kilo text editor from https://viewsourcecode.org/snaptoken/kilo/


### Raw Input and Output
CTRL_KEY = Set the upper 3 bits of character to 0, similar to what CTRL does in keyboard.
0x1b[2J = Escape sequence commands take arguments, which come before the command. In this case the argument is 2, which says to clear the entire screen. 
        <esc>[1J would clear the screen up to where the cursor is, and <esc>[0J would clear the screen from the cursor up to the end of the screen. Also, 0 is the default argument for J, so just <esc>[J by itself would also clear the screen from the cursor to the end.

Terminal size can be fetched from ioctl call with TIOCGWINSZ request.

### Todo: Add dirty flag for text modifications
