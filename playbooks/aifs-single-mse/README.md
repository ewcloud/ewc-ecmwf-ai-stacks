# AIFS Single MSE

Featuring the ECMWF AIFS Single MSE data-driven model. Find more information in <https://huggingface.co/ecmwf/aifs-single-1.0>

## Usage

  ```bash
  ansible-playbook -i inventory aifs-single-mse.yml
  ```

## Inputs

- `aifs_single_mse_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
- `aifs_single_mse_env_name`: Name of the environment containing the ECMWF toolbox. Default: aifs-single-mse
- `aifs_single_mse_create_ipykernel`: Boolean to create a system-wide kernel available. Default: yes
- `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
- `conda_user`: User owning the conda installation. Default: `root`
