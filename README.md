# SlsDetector: LLM-Based Misconfiguration Detection for AWS Serverless Computing

We provide code of our framework SlsDetector, evaluation baseline and dataset, and used dataset of data-driven approach.


## Code of SlsDetector

Our misconfiguration detection approach is implemented in the file "SlsDetector.py".

## Evaluation Baselines

Baseline 1: data-driven approach in the directory "DDmethod".

- Learn Used Patterns (save in the directory "Patterns"): 
    - The directory "Dataset" contains 701 configuration files from 658 serverless applications in AWS SAR.
    - The file "AWSupdate_data.ipynb" can learn the patterns from the dataset about configuration resource types, configuration entries, and configuration entry values.
    - The file "RuleMining.py" can learn the patterns from the dataset about configuration denpendencies among entries and values.
    - The code file "GeneralMethod.py" contains some general method implementations.
- Detector Configuration File:
    - The file "approachAWS.ipynb" is based on learned patterns to conduct misconfiguration detection for tested configuration files of the serverless application.

