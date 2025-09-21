# This is the codebase of ICLR anonymous submission.

## Overview
This code implements a variant of chain of thought (CoT) prompting
called Program Trace Prompting (PTP) that makes explanations more
observable while preserving the power, generality and flexibility of
CoT.  In PTP, few-shot CoT demonstrations are wrapped in a formal
syntax based on Python, and each prompt: 

 * identifies and names steps;

 * defines the input/output behavior of steps; and 

 * replaces CoT explanations of in-context examples with chains of
these formalized steps on the same examples.  

PTP is applicable to many tasks, achieving strong results on the 23
diverse tasks in the BIG-Bench Hard benchmark. More importantly, by
instrumenting explanations in this way, we enable new types of
analysis. In particular, we identify "non-local errors" (which
correspond to incorrectly learning the reasoning method illustrated in
the demonstrations) as an unaddressed issue in CoT learning, and we
present methods for verifying the "modularity" of steps in a CoT
explanation.

## Data

We are comparing PTP to the CoT prompts in [BBH
dataset](https://github.com/suzgunmirac/BIG-Bench-Hard)

## Training

Please refer to the `training` directory for detailed training procedures.


## Experimental Logs
We provide our sampled traces in ```training/data/data```, 
and include all experimental logs in ```training/evals```

