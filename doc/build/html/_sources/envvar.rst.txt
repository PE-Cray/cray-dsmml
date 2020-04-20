Environment Variables
=====================

The following environment variables affect the DSMML behavior.

::

   DSMML_VERSION_INFO
       If set, causes DSMML to display the Cray DSMML library version number as
       well as the build date information.

       Default: not enabled

   DSMML_ERROR_FILE

       Specifies the name of error file to be used for reporting the errors in
       DSMML. Only ```stderr``` and ```stdout``` are available as valid input
       options.

       Default: stderr

   DSMML_DEBUG_FILE

       Specifies the name of the file to be used for reporting the debug logs
       in DSMML. Only ```stderr``` and ```stdout``` are available as valid
       input options.

       Default: stderr

   DSMML_DEBUG_LEVEL

       Specifies the level for providing the debug log details. The following
       levels are available as valid input options, and their corresponding
       information level details are provided.

       Level:1 Only error reports
       Level:2 General high-level user-facing function entry information
       Level:3 High-level function entry information on all other functions
       Level:4 More details on each internal operation
       Level:5 Complete every possible log information

       Default: 0

   DSMML_DEBUG_RANKS

       Specifies the ranks on which the debug logs are to be retrieved. Multiple
       ranks can be combined using the (;) delimiter.

       Default: (All ranks are reported)

   DSMML_DEBUG_CATEGORIES

       Debug categories used to isolate and separate the log information. The
       following categories are available as input. Multiple categories can be
       combined using the (;) delimiter.

       init
       enter
       create
       allocate
       query
       numa

       Default: (All categories are reported)

