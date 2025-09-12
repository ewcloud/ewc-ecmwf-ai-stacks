# AIFS ENS CRPS

Featuring the ECMWF AIFS ENS CRPS data-driven model. Find more information in <https://huggingface.co/ecmwf/aifs-ens-1.0>

## Usage

  ```bash
  ansible-playbook -i inventory aifs-ens-crps.yml
  ```

## Inputs

- `aifs_ens_crps_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
- `aifs_ens_crps_env_name`: Name of the environment containing the ECMWF toolbox. Default: aifs-ens-crps
- `aifs_ens_crps_create_ipykernel`: Boolean to create a system-wide kernel available. Default: yes
- `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
- `conda_user`: User owning the conda installation. Default: `root`
