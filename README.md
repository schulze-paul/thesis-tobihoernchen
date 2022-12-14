# Thesis

Master Thesis on Reinforcement Learning with Anylogic

## Installation

For the Python part, just run 'pip install -r requirements.txt'. 

You can get Anylogic from their [website](https://www.anylogic.com/downloads/). Any version works, but there are limitations to some versions as stated in the [Alpyne docs](https://t-wolfeadam.github.io/Alpyne/_build/html/intro_getstarted.html).

JRE is also required, CUDA might be useful.

If you plan to work with certain libraries in Anylogic (like Material Handling), be aware that depending on the Anylogic version you might be required to move some .jar files. The procedure is described in the corresponding [issue on github](https://github.com/t-wolfeadam/Alpyne/issues/18).

## Structure

- [envs](./envs): Anylogic-models and exported .zips for training
- [exploration](./exploration): Collection of jupyter notebooks for running examples and training procedures 
    - [basics_re](./exploration/basics_re/):
        - [frozen_lake](./exploration/basics_re/frozen_lake.ipynb): Implementation of the [Deeplizard Reinforcement Learning Tutorial](https://www.youtube.com/watch?v=HGeI30uATws&list=PLZbbT5o_s2xoWNVdDudn51XM8lOuZ_Njv&index=9)
        - [agv_slipcourse](./exploration/basics_re/agv_slipcourse.py): Simple example of the environment from the [Anylogic Reinforcement Learning Tutorial](https://www.youtube.com/watch?v=NeQYsKADD_c) being played with keyboard inputs over alpyne.
        - [agv_slipcourse_q_learning](./exploration/basics_re/agv_slipcourse_q_learning.ipynb): Simple example of a q-learning-agent in the environment from the [Anylogic Reinforcement Learning Tutorial](https://www.youtube.com/watch?v=NeQYsKADD_c) being trained with alpyne.
        - [agv_slipcourse_dqn](./exploration/basics_re/agv_slipcourse_dqn.ipynb): Simple example of a dqn-learning-agent in the environment from the [Anylogic Reinforcement Learning Tutorial](https://www.youtube.com/watch?v=NeQYsKADD_c) being trained with alpyne.
        - [agv_slipcourse_stable_baselines](./exploration/basics_re/agv_slipcourse_stable_baslines.ipynb): Simple example of a PPO-learning-agent (from stable basleines 3) in the environment from the [Anylogic Reinforcement Learning Tutorial](https://www.youtube.com/watch?v=NeQYsKADD_c) being trained with alpyne.
    - [MiniMatrix](./exploration/MiniMatrix/): Different tests for the smaller MiniMatrix-Environment (smaller version of the final MatrixProduction)
- [thesis](./thesis): Everything that is referenced from the notebooks in [exploration](./exploration).
    - [dqn](./thesis/dqn/): reusable code from the [agv_slipcourse_dqn-example](./exploration/basics_re/agv_slipcourse_dqn.ipynb)
    - [envs](./thesis/envs): Gym-Environments for RL Training
    - [policies](./thesis/policies/): Deep-learning-models for RL-training
    - [pypeline_connectors](./thesis/pypeline_connectors/): Code used for running trained policies from anylogic with visualization
    - [q_learning](./thesis/q_learning/): reusable code from the [agv_slipcourse_q_learning-example](./exploration/basics_re/agv_slipcourse_q_learning.ipynb)