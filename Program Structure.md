# Program Structure

- function library shared between remove and restore

+ reader for info file
+ checker for checking files in and out (check in / check out)
  - composed of array of functions
  - reversed by flag
  - must be 1000% idempotent
+ error handler
+ interactive tool
+ logger (for verbose)

- option handling is local to calling file (remove and restore)


