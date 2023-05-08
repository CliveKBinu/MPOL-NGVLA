## Requirments
  - Get HPPC account
  - X11 software for GUI display from HPCC ( Install it in your local PC)
  - Install Termux in HPCC
    - This for running jupyterlab or python traning in the background 
  - Install conda enviroment in HPCC
  - Install python in HPCC
  - Install MPol  ($ pip install MPoL) in HPCC

  ## Steps
  ### Initial setup:
  - You need 2 terminals running, lets call them A and B 
  - On terminal A, log in using 
  
        ssh -Y -J <eraider_username>@ssh.ttu.edu <eraider_username>@quanah.hpcc.ttu.edu
        
  - Assuming you have installed conda, create a new conda env using
  
        conda create --name mpol  python=3.10
        
  - Now activate conda env using (Conda Cheat sheet:https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)
    
        conda activate mpol
    
  - Now install Tmux using:
  
        conda install tmux
   
  - Now start a tmux session using
  
        tmux
  
  - Now you are a tmux session, you can deattach from the session (not kill) using (Tmux cheat cheet :https://tmuxcheatsheet.com/)
  
      Ctrl + b + d
   
  - Also install Jupyternotebook or Jupyterlab using:
  
        conda install -c anaconda jupyter
              
    > or
    
        pip install jupyterlab
              
    > or
    
        conda install -c conda-forge jupyterlab
------------

### Opening Jupyternotebook / Jupyterlab
  - Now start an interactive sessision in quanah using the below command and go to the dir you will be working from  
  
        interactive -p matador -N 2
        
  - Then start a headless jupyter notebook server
        
        (Add command here after HPCC is back online)
        
  - Now follow the .ipynb file to use MPol ot the NGVLA data
      
