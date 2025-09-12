# AI Models

Featuring the most popular data driven forecast models such as Pangu Weather, Fourcastnet or graphcast. You may use the following ansible variables to customise this playbook:

## Usage

  ```bash
  ansible-playbook -i inventory ai-models.yml
  ```

## Inputs

You may use the following ansible variables to customize this playbook:

- `ai_models_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
- `ai_models_env_name`: Name of the environment containing the ECMWF toolbox. Default: ai-models
- `ai_models_create_ipykernel`: Boolean to create a system-wide kernel available. Default: yes
- `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
- `conda_user`: User owning the conda installation. Default: `root`
