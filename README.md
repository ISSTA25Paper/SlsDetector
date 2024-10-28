# SlsDetector: LLM-Based Misconfiguration Detection for AWS Serverless Computing

We provide code of our framework SlsDetector, evaluation baselines, and evaluation dataset.


## Code of SlsDetector

Our misconfiguration detection approach is implemented in the file "SlsDetector.py", which supports different LLMs.

## Evaluation Baselines

Baseline 1: data-driven approach in the directory "DDmethod".

- Learn Used Patterns (save in the directory "Patterns"): 
    - The directory "Dataset" contains 701 configuration files from 658 serverless applications in AWS SAR.
    - The file "AWSupdate_data.ipynb" can learn the patterns from the dataset about configuration resource types, configuration entries, and configuration entry values.
    - The file "RuleMining.py" can learn the patterns from the dataset about configuration denpendencies among entries and values.
    - The code file "GeneralMethod.py" contains some general method implementations.
- Detect Configuration File:
    - The file "approachAWS.ipynb" is based on learned patterns to conduct misconfiguration detection for tested configuration files of the serverless application.

Baseline 2: basic LLM-based approach.

- The baseline 2 - BL method is implemented in the file "BLmethod.py", which supports different LLMs.

## Evaluation Dataset

We construct this evalution dataset including configuration files without errors, configuration files with real-world errors, and configuration files with injected errors.

- The directory "configurations without errors" contains 52 correct configuration files, where 26 (naming from case 1 to case 26) are used to evaluate error-free configurations, while the remaining 26  (naming from case 27 to case 52) are reserved for generating configurations with injected errors.
    - The detailed information of these configuration files are described in the file "correct configurations.xlsx".
- The directory "configurations with real-world errors" contains 58 configuration files with real-world misconfigurations from GitHub.
    - The specific links of these configuration problems are provided in the file "realworld problem information.xlsx".
- The directory "configurations with injected errors" contains 26 configuration files with injected errors (case 27 to case 52).
    - The specific injected changes are provided in the file "injected configurations.xlsx".

The information of all configuration files with their ground-truth answers is summarized in the file "EvaluationConfigurationSummarization.xlsx".