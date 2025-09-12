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

License
-------

Apache 2.0.

Author Information
------------------

ECMWF for the European Weather Cloud
