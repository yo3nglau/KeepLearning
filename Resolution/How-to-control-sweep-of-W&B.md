## Resolution: How to control sweep of W&B

### Start

Initialize the sweep with the CLI, type the `PROJECT_NAME` and `CONFIG.yaml`:

```python
wandb sweep --project PROJECT_NAME CONFIG.yaml
```

After initialization, a particular `SWEEP_ID` will be generated.

Start the sweep agent with the `SWEEP_ID`:

```python
wandb agent ENTITY/PROJECT_NAME/SWEEP_ID
```

### Pause

Pause the sweep to temporarily stop running new runs:

```python
wandb sweep --pause ENTITY/PROJECT_NAME/SWEEP_ID
```

### Stop

Finish the sweep to stop running new runs and let currently running runs finish.

```python
wandb sweep --stop ENTITY/PROJECT_NAME/SWEEP_ID
```

**Note:** If you just want to temporarily pause your sweep and come back to resume later, you are supposed to use `Pause` rather than `Stop`, which, as far as I am concerned, is only executed when you think that the sweep thus far is enough and can be finished. Notwithstanding, you are still able to resume the stopped sweep by means of creating a new agent, as shown in `Resume`.

### Resume

Resume the **paused** sweep:

```python
wandb sweep --resume ENTITY/PROJECT_NAME/SWEEP_ID
```

Resume the **stopped** sweep:

```python
wandb sweep --resume ENTITY/PROJECT_NAME/SWEEP_ID
wandb agent ENTITY/PROJECT_NAME/SWEEP_ID
```

That means a new agent is provided to resume the sweep.

### Cancel

Cancel the sweep to kill all running runs and stop running new runs.

```python
wandb sweep --cancel ENTITY/PROJECT_NAME/SWEEP_ID
```

<br>

## Reference

[Initialize sweeps](https://docs.wandb.ai/guides/sweeps/initialize-sweeps)

[Start sweep agents](https://docs.wandb.ai/guides/sweeps/start-sweep-agents)

[Pause, resume, stop and cancel sweeps](https://docs.wandb.ai/guides/sweeps/pause-resume-and-cancel-sweeps)

