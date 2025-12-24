# 1. Create aiwp virtual environment and Install eccodes library

On milan:
```
module load anaconda/3-new
module load git/2.36.2
conda create -p ./env_aiwp python=3.12
conda activate ./env_milan
conda install -c conda-forge eccodes=2.42.0
bash install.sh
```

On login:
```
module load anaconda/3-new
module load git/2.36.2
conda create -p ./env_aiwp python=3.11
conda activate ./env_login
bash install.sh
pip install jax==0.5.2
```
# 2. How to submit a job?

After ssh to the login node (milan), run "sbatch main_job.sh" in the terminal. 

# 3. How to parallelize the jobs?

You may need to run the ai-models-gfs with different input arguments (date, forecast_lead, etc.). 

Seawulf use the tool "GNU parallel" to parallelize the jobs. Google it to figure out how it works.



# physics-constrained-ai-weather-forecast
