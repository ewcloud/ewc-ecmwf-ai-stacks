# Anemoi Framework

Leverage the Anemoi framework to develop and run your AI-models or manage datasets. See <https://anemoi.readthedocs.io/en/latest/> for more information

## Usage

  ```bash
  ansible-playbook -i inventory anemoi.yml
  ```

## Inputs

You may use the following ansible variables to customise this playbook:

- `anemoi_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
- `anemoi_env_name`: Name of the environment containing the ECMWF toolbox. Default: anemoi
- `anemoi_create_ipykernel`: Boolean to create a system-wide kernel available. Default: yes
- `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
- `conda_user`: User owning the conda installation. Default: `root`
