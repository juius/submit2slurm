submit2slurm
=============

Setup
------

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

