# Self-Reflection Helps Prompt Refinement: Prompt Reflection

**Table of Contents**

- [Setup](#setup)
- [BBH](#bbh)
- [GSM8K](#gsm8k)
- [HumanEval](#humaneval)
- [MATH](#math)



## Setup

We use the OpenAI API to asynchronously query the models.  We follow a general file structure in each benchmark:

* 'RIR.py' : is the main file that needs to be run, to run the benchmark
* 'task_init.py' : used to initilize the self-refining
* 'task_iterate.py' : used to get the next iteration in the self-refining pipeline
* 'feedback.py' : used to provide feedback in the self-refining pipeline
* 'outputs' : stores the outputs

An API key needs to be provided for the respective benchmarks. It is a parameter that needs to specified in the 'RIR.py' file

Depending on your default settings, you may need to adjust the PYTHONPATH for the benchmark. This can be done by opening the respective benchmark and running: 

```sh
export PYTHONPATH="$PWD"
```

## BBH

* Run all test cases with:

```sh
python RIR.py
```


## GSM8K

* Run the benchmark with:

```sh
python RIR.py
```

## HumanEval

* Run the benchmark with:

```sh
python RIR.py
```

* To evalute the output use:

```sh
python human_eval/evaluate_functional_correctness.py outputs/FILENAME.jsonl
```
* This will generate a FILENAME.jsonl_results.jsonl file and report the accuracy in the terminal
  
## MATH

* Run the benchmark with:

```sh
python RIR.py
```
