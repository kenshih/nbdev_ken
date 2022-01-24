# nbdev_ken
https://kenshih.github.io/nbdev_ken/

# toc

- [nbdev_ken](#nbdev_ken)
- [toc](#toc)
- [start](#start)
- [how this was set up](#how-this-was-set-up)

# start

```
# use environment.yml to install in ./envs
conda env create -f environment.yml # todo check
# enter envs environment
conda activate ./envs
# change path
export PATH=/Users/ken/wk/experiments/ml/nbdev_ken/envs/bin:$PATH
```

refs: 
- https://jekyllrb.com/

# how this was set up

This env was created in this directory with:
```
conda create -c fastchan --prefix ./envs jupyterlab fastai nbdev python=3.10
# create environment
conda env export > environment.yml

# mutate .condarc
conda config --set env_prompt '({name})'

# reinstalled ruby to 3.x for jekyll
\curl -sSL https://get.rvm.io | bash
source /Users/ken/.rvm/scripts/rvm
rvm install ruby
rvm reload
gem install bundler jekyll

```
Referencing...
- https://nbdev.fast.ai/tutorial.html#Set-up-Your-Jupyter-Server
- https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-channels.html#
- https://www.fast.ai/2021/07/15/fastconda/