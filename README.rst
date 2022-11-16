submit2slurm
=============

Setup
------
SLURM default parameters like ``partition`` and ``time`` are set in ``slurm_params_<cluster>.txt``
Here, ``slurm_params_steno.txt`` and ``slurm_params_sunray.txt`` are available.

.. code-block:: sh
  
  cp submit ~/bin/.
  PWD=`pwd`
  sed -i -e "s|source .*|source $PWD/slurm_params_steno.txt|" ~/bin/submit
  chmod +x ~/bin/submit
    
Usage
------

.. code-block:: sh
    
    submit python <file>.py
    
    submit gaussian <file>.com

Flags
^^^^^^
All flags are optional

-c int        Number of CPUs to use. Default=2
-m int        Memory in GB. Default=4
-a            Optional arguments parsed to submitted script. Default=None
