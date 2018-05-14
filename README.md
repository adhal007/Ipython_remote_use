
# Ipython_remote_use
# First Have both your remote machine and local machine set up with anaconda distibution
# In remote host navigate to your /home/user/anaconda/bin , where your jupyter kernel is located

jupyter notebook --no-browser --port=8889

# you should leave the this open

ssh -N -f -L localhost:8888:localhost:8889 username@your_remote_host_name

# make sure to change `username` to your real username in remote host
# change `your_remote_host_name` to your address of your working station
# Example: ssh -N -f -L localhost:8888:localhost:8889 adhal@cabernet.genomecenter.ucdavis.edu

# Finally you will be asked for a token authentication. Use the token for localhost:8889 from remote machine to run on your local machine.
