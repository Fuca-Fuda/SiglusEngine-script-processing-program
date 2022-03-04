# SiglusEngine-script-processing-program

In the process of script processing for SiglusEngine, we encountered many situations that required editing with text processing programs, such as the need to put character names and dialogues on one line, and to filter out program command lines in scripts, etc. We have now completed a more complete script processing program for SiglusEngine only, and we can later use this program for many This program can be used to process scripts of many engines.

This program has only one main.cpp that makes sense, which has a total of four function functions and three call functions for easy execution, which are implemented as follows.

Deal_Txt(): the script file is processed, and the character name and dialogue content are put on one line by judging the left bracket, while all the program instruction lines are filtered out by judging whether the first character is an English character or not, and the result of the execution is that the script file is split into two files, the first one is a text-only translation file for convenient translation, and the second one is used to save the program instruction and its line number The first is a text-only translation file for easy translation, and the second is an additional file for saving the program instructions and their lines.

Restore_Txt(): Restore the two files just generated, and reassemble them into the original script file, but the text part of it has been translated, the new script file generated has no formatting difference with the original script file, and can be directly used for the upper-level package operation.

Change_Name(): use rename function to modify the file name in batch, here is mainly for Siglus engine related unpacking tools to generate the extended suffix problem, this program can set the file suffix length to delete the number of bits, for example, ".ss.txt.out", delete to direct out" to ".ss.txt" which can be packaged directly. However, rename can also perform other complex operations, and can be modified flexibly if needed.

The *_Do function is the entry point for executing the above functions. The Do series of functions have a file loop that can operate on all script files in the entire folder.
