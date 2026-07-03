# Auto-NBA Parameter Experiments

This project explores how different Auto-NBA configuration parameters affect search time, training time, and model accuracy.

Auto-NBA is an AI search tool that searches across network architecture, bitwidths, and accelerator/hardware configurations. This project focused on changing configuration parameters, running experiments in Google Colab, and comparing the results.

## Project Overview

The goal of this project was to better understand how Auto-NBA configuration settings affect performance. The experiments measured:

- Search time
- Training time
- Training accuracy

The project used CIFAR-10, a 5% training portion, 25 search epochs, 25 training epochs, and a Google Colab T4 GPU.

## Technologies

- Python
- Google Colab
- Machine Learning
- Neural Architecture Search
- Auto-NBA configuration files
- Arduino / Embedded AI workflow

## Experiments

- Bitwidth search space
- Fixed bitwidth values
- Alpha / beta weights
- Efficiency metric: latency vs. FLOPs
- Channel list sizes
- Number of layers

## Results Summary

| Experiment | Main Finding |
|---|---|
| Bitwidth Search Space | Larger bitwidth search spaces increased search time but improved accuracy. |
| Fixed Bitwidth Values | 8-bit produced the highest accuracy among fixed bitwidth runs. |
| Alpha/Beta Weights | Lower alpha/beta values produced higher accuracy in the tested runs. |
| Efficiency Metric | Latency had better training time, while FLOPs had faster search time. |
| Channel List | Larger channel sizes improved accuracy but increased search time. |
| Number of Layers | Changing the layer list broke Auto-NBA during testing. |

## Example Result: Bitwidth Search Space

| Configuration | Search Time | Train Time | Accuracy |
|---|---:|---:|---:|
| [4] | 55 min | 46 min | 77.917 |
| [4, 6] | 1 hr 35 min | 40 min | 81.647 |
| [4, 6, 8] | 2 hr 17 min | 41 min | 85.536 |

Larger bitwidth search spaces improved model accuracy, but also increased search time.

## Repository Contents

- `configs/` - Search and training configuration files used for each experiment
- `notebook/` - Google Colab notebook used to set up and run Auto-NBA
- `docs/` - Final project report
- `slides/` - Final presentation slides

## Arduino / Embedded AI Note

Arduino hardware was used as part of the embedded AI course workflow. The Auto-NBA parameter experiments were run through Google Colab, while the Arduino component supported the broader embedded AI project context.

## Notes

This was a group coursework project by Jaden Ziga, Jacob Wheeler, and Ryan Hastie.

This repository does not claim ownership of the original Auto-NBA tool. It contains experiment configuration files, project documentation, and analysis created for coursework.

Full experiment tables and analysis are available in the final report and presentation located in the `docs/` and `slides/` folders.
