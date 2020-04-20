Compile and Launch
==================

To invoke the compiler for all applications, including standalone DSMML
applications, use either the cc, CC, or ftn command. Do not use any
vendor-specific compiler commands such as pgcc, as this may result in
undefined behavior.

Example:

In the example below, an application is first compiled, and the
resulting executable is then launched using 1 process:

.. code:: bash

   cc -o test_dsmml test_dsmml.c
   srun -n 1 ./test_dsmml

See srun(1) man page for more information.

