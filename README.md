$ yamllint playbook.yaml 

$ ansible-lint playbook.yaml 

$ ansible-playbook --syntax-check -i hosts playbook.yaml  

$ ansible-playbook -i hosts --private-key ~/.ssh/ansible_id_rsa -u ansible playbook.yaml

