EWC Automation of ECMWF AI stacks
=================================

This repository contains Ansible playbooks for customising EWC instances with specific AI stacks, including:

- ai-models: featuring the most popular data driven forecast models such as Pangu Weather, Fourcastnet or graphcast.
- aifs-single-mse: featuring the ECMWF AIFS Single data-driven model
- aifs-ens-crps: featuring the ECMWF AIFS ENS CRPS data-driven model
- Anemoi framework: leverage the Anemoi framework to develop and run your AI-models or manage datasets.
- ML Basic: featuring an environment with the main machine learning packages like scikit-learn or torch.

Getting started
---------------

- Install ansible and other dependencies. You may want to do it in its own virtual environment (`pip install -r requirements.txt`)
- Fetch the external requirements

  ```bash
  ansible-galaxy role install -r requirements.yml roles/
  ```

- Define your inventory in `inventory`
- Run the apropriate playbook

  ```bash
  ansible-playbook -i inventory playbookname.yml
  
  ```

Available Playbooks
-------------------

- **ml-basic**. featuring an environment with the main machine learning packages like scikit-learn or torch. You may use the following ansible variables to customise this playbook:
  - `ml_basic_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
  - `ml_basic_env_name`: Name of the environment containing the ECMWF toolbox. Default: ai-models
  - `ml_basic_create_ipykernel`: Boolean to create a system-wide kernel available. Default: yes
  - `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
  - `conda_user`: User owning the conda installation. Default: `root`

  Example usage:

  ```bash
  ansible-playbook -i inventory ml-basic.yml
  ```
  
- **ai-models**. Featuring the most popular data driven forecast models such as Pangu Weather, Fourcastnet or graphcast. You may use the following ansible variables to customise this playbook:
  - `ai_models_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
  - `ai_models_env_name`: Name of the environment containing the ECMWF toolbox. Default: ai-models
  - `ai_models_create_ipykernel`: Boolean to create a system-wide kernel available. Default: yes
  - `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
  - `conda_user`: User owning the conda installation. Default: `root`

  Example usage:

  ```bash
  ansible-playbook -i inventory ai-models.yml
  ```

- **aifs-single-mse**. Featuring the ECMWF AIFS Single data-driven model. You may use the following ansible variables to customise this playbook:
  - `aifs_single_mse_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
  - `aifs_single_mse_env_name`: Name of the environment containing the ECMWF toolbox. Default: aifs-single-mse
  - `aifs_single_mse_create_ipykernel`: Boolean to create a system-wide kernel available. Default: yes
  - `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
  - `conda_user`: User owning the conda installation. Default: `root`

  Example usage:

  ```bash
  ansible-playbook -i inventory aifs-single-mse.yml
  ```

- **aifs-single-mse**. Featuring the ECMWF AIFS ENS CRPS data-driven model. You may use the following ansible variables to customise this playbook:
  - `aifs_ens_crps_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
  - `aifs_ens_crps_env_name`: Name of the environment containing the ECMWF toolbox. Default: aifs-ens-crps
  - `aifs_ens_crps_create_ipykernel`: Boolean to create a system-wide kernel available. Default: yes
  - `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
  - `conda_user`: User owning the conda installation. Default: `root`

  Example usage:

  ```bash
  ansible-playbook -i inventory aifs-ens-crps.yml
  ```

- **anemoi-framework**. Leverage the Anemoi framework to develop and run your AI-models or manage datasets. You may use the following ansible variables to customise this playbook:
  - `anemoi_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
  - `anemoi_env_name`: Name of the environment containing the ECMWF toolbox. Default: anemoi
  - `anemoi_create_ipykernel`: Boolean to create a system-wide kernel available. Default: yes
  - `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
  - `conda_user`: User owning the conda installation. Default: `root`

  Example usage:

  ```bash
  ansible-playbook -i inventory anemoi.yml
  ```

License
-------

Apache 2.0.

Author Information
------------------

ECMWF for the European Weather Cloud
