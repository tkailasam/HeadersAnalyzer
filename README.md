Headers Analyzer
================

Headers Analyzer is a Burp extension written in Python that making use of the "Passive Scanner" functionality checks for:

  - Headers that might disclose some interesting information. 
  - Missing security headers.
  - Misconfigured security headers.

Issues found will be reported and added to the passive scanner tab in a similar way to the native issues reported by Burp.

The extension will add a new tab to Burp's UI to allow the user to configure it, including the following aspects:

  - Select what kind of headers the extension should analyze.
  - Boring headers, a list of boring headers that the extension will omit.
  - Export the results in a "report friendly" format.

An additional "BoringHeaders.txt" file is included apart from the extension. This file includes a predefined list of boring headers that might prove useful for the user. 

Screenshots
-----------
Extension tab:

![Alt text](/Screenshots/1.jpg?raw=true "Extension Tab")

Flagged issues:

![Alt text](/Screenshots/2.jpg?raw=true "Flagged Issues")


Version
-------

0.1


Installation
--------------

Jython 2.7+ is needed for this extension to work properly, so remember to set it up in Burp before adding the extension.
After that, just add a new extension in the "Extensions" tab, choose "Python" as the extension type, and point to the "HeadersAnalyzer.py" file.

The first time you load the extension, the "Boring Headers" list will be empty, a file with default boring headers can be found at:
https://github.com/Dionach/HeadersAnalyzer/blob/master/BoringHeaders.txt. 

The extension will save the current settings before Burp is closed, and restore them once the extension is loaded again.

Check the "Output" and "Errors" tabs for possible feedback.
