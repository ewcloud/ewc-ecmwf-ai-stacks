# ML Basic Stack

Featuring an environment with the main machine learning packages like scikit-learn or torch.

## Usage

  ```bash
  ansible-playbook -i inventory ml-basic.yml
  ```

## Inputs

- `ml_basic_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
- `ml_basic_env_name`: Name of the environment containing the ECMWF toolbox. Default: ai-models
- `ml_basic_create_ipykernel`: Boolean to create a system-wide kernel available. Default: yes
- `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
- `conda_user`: User owning the conda installation. Default: `root`
