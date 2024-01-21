---
layout: page
title: competetive Open Ai
description: Meta-Learning in Nonstationary and Competitive Environments with code and paper
img: assets/img/robosumo1.gif
importance: 1
category: my favorites
related_publications: true
---

RoboSumo
========

This repository contains a set of competitive multi-agent environments used in the paper [Continuous Adaptation via Meta-Learning in Nonstationary and Competitive Environments](https://arxiv.org/abs/1710.03641).


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/robosumo1.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/robosumo2.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    this is AI playing Wrestling Spiders in the red...
</div>



## Installation this project :

RoboSumo depends on `numpy`, `gym`, and `mujoco_py>=1.5` (if you haven't used MuJoCo before, please refer to [the installation guide](https://github.com/openai/mujoco-py)).
Running demos with pre-trained policies additionally requires `tensorflow>=1.1.0` and `click`.

The requirements can be installed via [pip](https://pypi.python.org/pypi/pip) as follows:

```bash
$ pip install -r requirements.txt
```

To install RoboSumo, clone the repository and run `pip install`:

```bash
$ git clone https://github.com/openai/robosumo
$ cd robosumo
$ pip install -e .
```

## Demos

You can run demos of the environments using `demos/play.py` script:

```bash
$ python demos/play.py
```

The script allows you to select different opponents as well as different policy architectures and versions for the agents.
For details, please refer to the help:

```bash
$ python demos/play.py --help

Usage: play.py [OPTIONS]

Options:
  --env TEXT                    Name of the environment.  [default: RoboSumo-Ant-vs-Ant-v0]
  --policy-names [mlp|lstm]...  Policy names.  [default: mlp, mlp]
  --param-versions INTEGER...   Policy parameter versions.  [default: 1, 1]
  --max_episodes INTEGER        Number of episodes.  [default: 20]
  --help                        Show this message and exit.
```

