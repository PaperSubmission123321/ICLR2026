## SFT
### Data Preparetion
To prepare data for SFT, refer to ``data/scripts/process_sft_data.py``. After preprocessing, use ``data/scripts/push_to_hub.sh`` to upload the dataset to your repository.

Next, check ``examples/data_preprocess/ptp_sft.py`` for guidance on formatting the data into the verl format.

### Training
Plrease refer to ```experiment/sft.sh``` for Stage-1 Supervised Fine-Tuning. Ensure that all file paths are correctly adjusted to match your environment.

To fine-tune SSRMs, verify that the appropriate ``chat_template`` is specified in ``verl/trainer/config/sft_trainer.yaml``.


## RLVR
### Data Prepartion
We will release the MedCalcV2 dataset publicly. For reproducibility, please refer to ``examples/data_preprocess/ptp_rl.py`` to convert the data into the verl format. The [DAPO Math](https://huggingface.co/datasets/open-r1/DAPO-Math-17k-Processed) set can also be used for experimentation.

### Training
For Stage-2 RLVR, refer to ``scripts/grpo.sh`` and modify the paths as necessary.


## Prompted Models
Before using prompted models, set the PYTHONPATH:
```shell
export PYTHONPATH="${PYTHONPATH}:../"
```

After setting up, please refer to ```training/data/scripts/sample_trace.sh```
for how to sample traces.

We provide our sampled traces in ```training/data/data```, 
and include all experimental logs in ```training/evals```

